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

**Относится к**: Outlook 2013 | Outlook 2016 
  
При отправке сообщения поставщик транспорта может создать файл, который будет содержать сообщение во время передачи. Затем интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) обвязывают файл. Затем поставщик транспорта использует методы [ITnef](itnefiunknown.md) для записи свойств сообщения в поток в формате с тегами, который позволяет принимающим поставщикам транспорта легко декодировать свойства. 
  
**Чтобы представить все сообщение в одном файле**
  
1. Получите объект TNEF, передав [объект IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и сообщение в [функцию OpenTnefStreamEx.](opentnefstreamex.md) 
    
2. Получите список всех определенных свойств сообщения, вызывая метод [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
    
3. Используйте [методы IMAPIProp,](imapipropiunknown.md) чтобы исключить все свойства, поддерживаемые системой обмена сообщениями. В соответствующее время запишите эти свойства в систему обмена сообщениями в формате, требуемом системой обмена сообщениями. 
    
4. Вызовите [ITnef::AddProps,](itnef-addprops.md) чтобы закодировать оставшиеся свойства, включая все вложения. 
    
5. Вызовите [метод ITnef::Finish,](itnef-finish.md) чтобы закодировать сообщение в поток TNEF после того, как будут добавлены все запрашиваемые свойства. 
    
6. Вызовите [метод ITnef::OpenTaggedBody,](itnef-opentaggedbody.md) чтобы получить помеченный текст сообщения. Этот помеченный текст заносит в систему обмена сообщениями с помощью методов из интерфейса OLE [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
7. Вызовите [метод IUnknown::Release,](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) чтобы освободить объект **ITnef.** 
    
**Обработка входящий TNEF-сообщения**
  
1. Получите объект сообщения MAPI из пула MAPI и запишите свойства загона сообщения в новое сообщение MAPI.
    
2. Создание и инициализация [объекта IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для хранения данных TNEF из входящего сообщения. 
    
3. Передав сообщение MAPI и [объект IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) [функции OpenTnefStreamEx.](opentnefstreamex.md) 
    
4. Декодирует сведения в данных TNEF, вызывая метод [ITnef::ExtractProps.](itnef-extractprops.md) 
    
   > [!NOTE]
   > Все, что декодировали с помощью **ExtractProps,** перезаписывание свойств, декодирования из конверта входящих сообщений. То есть извлеченные свойства TNEF переопишют существующие свойства в сообщении. 
  
5. Обработать помеченный текст сообщения, вызывая [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) и разбор текста для восстановления позиций вложений. 
    
6. Сохраните сообщение, вызывая [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)
    
7. Освободите объект TNEF, вызывая метод [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) 
    

