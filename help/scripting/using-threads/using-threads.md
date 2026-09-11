---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: Aprenda a usar threads em scripts Substance 3D Designer Python para processamento e desempenho paralelos.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usando threads
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Usando threads

É possível que plug-ins <b>criem threads</b> usando o módulo de threading do Python *ou* Qt para classes relacionadas a threads do Python.

Isso pode ser útil para executar operações de processamento em segundo plano ou de E/S enquanto o Designer está em execução.

É importante observar que a maioria das classes e métodos na API Python do Designer podem *apenas* ser chamados do <b>thread principal do aplicativo</b>. Dessa forma, se você deseja fazer qualquer modificação em qualquer gráfico que esteja aberto atualmente no Designer, é necessário fazê-las a partir do thread do aplicativo principal.

Uma solução possível é usar o <b>QThread</b> e as <b>conexões em fila</b>, como no exemplo a seguir:

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
