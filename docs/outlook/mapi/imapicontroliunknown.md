---
title: IMAPIControl IUnknown
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414041"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Включает и отключает управление кнопками и выполняет задачи, когда пользователь клиентского приложения щелкает включенную кнопку управления. Поставщики служб реализуют объекты управления, чтобы создавать настраиваемые кнопки на диалоговых полях, например листы свойств конфигурации, которые определяются с помощью таблиц отображения. 
  
Дополнительные сведения о работе с таблицами отображения и объектами управления см. в таблице [Display Tables.](display-tables.md)
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты управления  <br/> |
|Реализовано в:  <br/> |Поставщики служб  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIControl  <br/> |
|Тип указателя:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке управления кнопками.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Выполняет такую задачу, как отображение диалогового окна или запуск программной операции, когда пользователь клиентского приложения нажимает кнопку управления.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Извлекает значение, которое указывает, включено или отключено управление кнопкой.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

