---
title: Кодирование сообщения с использованием формата TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336703"
---
# <a name="encoding-a-message-with-tnef"></a>Кодирование сообщения с использованием формата TNEF

**Область применения**: Outlook 2013 | Outlook 2016 
  
При отправке сообщения поставщик транспорта может создать файл, который используется для отправки сообщения. Затем интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) обмотается вокруг файла. Затем поставщик транспорта использует методы [ITnef](itnefiunknown.md) для записи свойств сообщений в поток в помеченном формате, который позволяет легко декодировать свойства принимающих поставщиков транспорта. 
  
**Для представления всего сообщения в одном файле**
  
1. Получение объекта TNEF путем передачи [объекта IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и сообщения в функцию [OpenTnefStreamEx.](opentnefstreamex.md) 
    
2. Получите список всех определенных свойств для сообщения, позвонив по [методу IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
    
3. Используйте [методы IMAPIProp,](imapipropiunknown.md) чтобы исключить все свойства, поддерживаемые системой обмена сообщениями. В соответствующее время напишите эти свойства в систему обмена сообщениями в формате, требуемом системой обмена сообщениями. 
    
4. Вызов [ITnef::AddProps для](itnef-addprops.md) кодирования оставшихся свойств, включая все вложения. 
    
5. Вызов метода [ITnef::Finish,](itnef-finish.md) чтобы закодировать сообщение в поток TNEF после того, как будут добавлены все запрашиваемые свойства. 
    
6. Чтобы получить помеченный текст сообщения, позвоните по методу [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md) Этот помеченный текст выписано в систему обмена сообщениями с помощью методов из интерфейса OLE [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
7. Вызов метода [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) для выпуска **объекта ITnef.** 
    
**Обработка входящие сообщения TNEF**
  
1. Получите объект сообщения MAPI из пульпера MAPI и напишите свойства загона сообщений в новое сообщение MAPI.
    
2. Создание и инициализация [объекта IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для хранения данных TNEF из входящего сообщения. 
    
3. Передай сообщение MAPI и [объект IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) функции [OpenTnefStreamEx.](opentnefstreamex.md) 
    
4. Расшифровка сведений в данных TNEF с помощью метода [ITnef::ExtractProps.](itnef-extractprops.md) 
    
   > [!NOTE]
   > Все, что декодировали **в ExtractProps,** будет перезаписывать свойства, декодироваться из конверта входящих сообщений. То есть извлеченные свойства TNEF переопишет существующие свойства в сообщении. 
  
5. Обработать помеченный текст сообщения, позвонив [в ITnef::OpenTaggedBody](itnef-opentaggedbody.md) и разбор текста для восстановления позиций вложений. 
    
6. Сохраните сообщение, позвонив [в IMAPIProp::SaveChanges.](imapiprop-savechanges.md)
    
7. Отпустите объект TNEF, позвонив [методу IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) 
    

