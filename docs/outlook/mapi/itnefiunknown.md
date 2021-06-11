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
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428517"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет методы инкапсулации свойств MAPI, которые не поддерживаются системой обмена сообщениями, в двоичные потоки, которые могут быть присоединены к сообщениям. Формат, используемый для этой инкапсуляции, Transport-Neutral формат инкапсуляции (TNEF). После получения сообщения, которое включает вложение TNEF, целевой поставщик транспорта или клиентное приложение MAPI можно восстановить свойства из вложения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Tnef.h  <br/> |
|Подвергается:  <br/> |Объекты TNEF  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики транспорта, поставщики магазинов сообщений и шлюзы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_ITNEF  <br/> |
|Тип указателя:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Позволяет поставщику услуг вызова или шлюзу добавлять свойства в инкапсуляцию сообщения или вложения.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Извлекает свойства из инкапсуляции TNEF.  <br/> |
|[Finish](itnef-finish.md) <br/> |Завершает обработку всех операций TNEF, которые находятся в очереди и ожидаются.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Открывает интерфейс потока в тексте инкапсулированного сообщения.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Задает значение одного или более свойств для инкапсулированного сообщения или вложения без изменения исходного сообщения или вложения.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Кодирует представление таблицы получателей сообщения в потоке данных TNEF для сообщения.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Обрабатывает отдельные компоненты из сообщения по одному в поток TNEF.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

