---
title: Разработка клиентского приложения MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410037"
---
# <a name="developing-a-mapi-client-application"></a>Разработка клиентского приложения MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения MAPI написаны с клиентского интерфейса MAPI, ориентированного на объект. Клиенты MAPI взаимодействуют с одной или более системами обмена сообщениями через подсистему MAPI и поставщиков услуг, совместимых с MAPI. Это взаимодействие может происходить разными способами; существует огромное разнообразие клиентских приложений. Большинство клиентов являются клиентами обмена сообщениями, либо интегрируя обмен сообщениями в установленный набор функций, либо выполняя функции обмена сообщениями в качестве основной функции. Другие функции, которые могут предоставлять клиенты MAPI, включают администрирование профилей или управление адресной книгой и хранилищем сообщений.
  
Все клиенты обмена сообщениями инициализируют библиотеки MAPI и начинают сеанс **с** подсистемы MAPI. Дополнительные сведения см. [в дополнительных сведениях о доступе к объектам с помощью сеанса.](accessing-objects-by-using-the-session.md) После того как сеанс установлен, клиент может:
  
- Обработка исходяющих сообщений, в том числе ответов, переадранных сообщений и ретранслиссий.
    
- Обработка входящих сообщений.
    
- Обрабатывайте хранилище сообщений, открывая папки и сообщения, создавая, изменяя, копируя и отправляя сообщения, отслеживая беседы и поиск одной или более папок.
    
- Обрабатывайте адресную книгу путем создания и изменения получателей, размещения записей и обхода иерархии контейнеров.
    
- Обработка поставщика транспорта путем выполнения перенастройки, настройки параметров и порядка транспортировки и отправки сообщений по запросу.
    
- Обработка уведомлений о событиях.
    
- Обработка форм.
    
- Обработка профилей и служб сообщений.
    
Используйте разделы в этом разделе, чтобы помочь вам реализовать эти основные задачи и конкретные функции, которые сделают ваш клиент MAPI уникальным.
  

