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
ms.openlocfilehash: 80acb1a1e4663a68efc4692ab67ec27bc369f4b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566518"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Включает и отключает элемент управления button и выполняет щелчку клиентского приложения включено элемента управления. Поставщики услуг реализовать объекты элементов управления для создания настраиваемых кнопок в диалоговых окнах, таких как страницы свойств конфигурации, определенные с помощью таблиц отображения. 
  
Дополнительные сведения о том, как для работы с таблицами отображения и управлять объектами можно [Отображение таблиц](display-tables.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объекты элементов управления  <br/> |
|Реализованный:  <br/> |Поставщики услуг  <br/> |
|Вызывается:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIControl  <br/> |
|Тип указателя:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего элемента управления кнопка.  <br/> |
|[Активация](imapicontrol-activate.md) <br/> |Выполняет задачи, как отображение диалогового окна или запуск программный операции при нажатии элемента управления кнопка пользователе клиентского приложения.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Получает значение, указывающее, включено ли элемент управления button.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

