---
title: Имапиконтрол IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280143"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Включает и отключает элемент управления "Кнопка" и выполняет задачи, когда пользователь клиентского приложения щелкает включенный элемент управления. Поставщики услуг реализуют объекты управления для создания настраиваемых кнопок в диалоговых окнах, например на страницах свойств конфигурации, которые определяются с помощью отображения таблиц. 
  
Дополнительные сведения о том, как работать с таблицами отображения и объектами управления, можно найти в разделе [Display Tables](display-tables.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты элементов управления  <br/> |
|Реализовано в:  <br/> |Поставщики служб  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапиконтрол  <br/> |
|Тип указателя:  <br/> |ЛПМАПИКОНТРОЛ  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке элемента управления "Кнопка".  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Выполняет задачу, например отображение диалогового окна или запуск программной операции, когда пользователь клиентского приложения щелкает элемент управления "Кнопка".  <br/> |
|[State](imapicontrol-getstate.md) <br/> |Получает значение, которое указывает, включен ли элемент управления "Кнопка" или отключен.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

