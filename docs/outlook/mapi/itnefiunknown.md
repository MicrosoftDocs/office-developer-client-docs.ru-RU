---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e8267b254648870cea4e16b4dea0e9c92e316fb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809635"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**Относится к**: Outlook 
  
Предоставляет методы для инкапсуляции свойства MAPI, не поддерживаемые системой обмена сообщениями в двоичные потоки, которые можно присоединить к сообщениям. Формат, используемый для этой инкапсуляция — Transport-Neutral Encapsulation формата TNEF. Целевой поставщика транспорта или на основе MAPI клиентское приложение можно, получив сообщение, содержащее вложения TNEF, восстановить свойства из вложения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF.h  <br/> |
|Предоставляемые:  <br/> |Объекты TNEF  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики транспорта, поставщиков хранилища сообщений и шлюзов  <br/> |
|Идентификатор интерфейса:  <br/> |IID_ITNEF  <br/> |
|Тип указателя:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Позволяет вызова поставщика услуг или шлюза добавить свойства к инкапсуляция вложения или сообщения.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Извлекает свойства из инкапсуляция TNEF.  <br/> |
|[Готово](itnef-finish.md) <br/> |По завершении обработки для всех операций TNEF в очереди и ожидание.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Открывает интерфейс потока на основе текста инкапсулированное сообщение.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Задает значение одного или нескольких свойств для инкапсулированное сообщение или вложение без изменения исходного сообщения или вложения.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Кодирует представления для таблицы получателей сообщения в потоке данных TNEF для сообщения.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Обрабатывает отдельные компоненты из сообщения одно за раз в поток TNEF.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

