---
title: Кодировка сообщение с TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382528"
---
# <a name="encoding-a-message-with-tnef"></a>Кодировка сообщение с TNEF

**Относится к**: Outlook 2013 | Outlook 2016 
  
При отправке сообщения поставщика транспорта можно создать файл, который используется для хранения сообщения во время передачи. Рассмотрим процедуру интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) является переход через файл. Поставщика транспорта затем использует методы [ITnef](itnefiunknown.md) для записи свойств сообщения поток в виде с тегами, включает свойства для декодирования легко получающей поставщиками транспорта. 
  
**Для представления все сообщение в одном файле**
  
1. Получение объекта TNEF, передав объект [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и сообщение в функцию [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Получите список всех свойств, определенных для сообщения путем вызова метода [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
3. Используйте методы [IMAPIProp](imapipropiunknown.md) , чтобы исключить все свойства, поддерживаемые системой обмена сообщениями. Во время запись этих свойств в системе обмена сообщениями в формате, необходимые для системы обмена сообщениями. 
    
4. Вызов [ITnef::AddProps](itnef-addprops.md) для кодирования остальные свойства, включая все вложения. 
    
5. Вызовите метод [ITnef::Finish](itnef-finish.md) для кодирования сообщений в поток TNEF после добавления все запрошенные свойства. 
    
6. Вызовите метод [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) получает текст с тегами сообщения. Этот текст с тегами записывается в системе обмена сообщениями, с помощью методов из интерфейса OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
    
7. Вызовите метод [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) для освобождения объекта **ITnef** . 
    
**Для обработки входящего сообщения в формате TNEF**
  
1. Получите объект MAPI сообщения из очереди MAPI и запись свойств заголовка сообщения в новое сообщение MAPI.
    
2. Создание и инициализация объекта [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для хранения данных TNEF из входящего сообщения. 
    
3. Передача сообщений MAPI и объект [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) функции [OpenTnefStreamEx](opentnefstreamex.md) . 
    
4. Сведения, приведенные в данных TNEF декодирования путем вызова метода [ITnef::ExtractProps](itnef-extractprops.md) . 
    
   > [!NOTE]
   > Все действия по **ExtractProps** свойства, декодированных из конверт входящие сообщения будут перезаписаны. То есть извлеченные свойства TNEF будет перезаписывать существующие свойства в сообщении. 
  
5. Процедура текст с тегами сообщения путем вызова [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) и синтаксический анализ текста для восстановления положения вложения. 
    
6. Сохраните сообщение, путем вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
7. Освободите объект TNEF путем вызова метода [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . 
    

