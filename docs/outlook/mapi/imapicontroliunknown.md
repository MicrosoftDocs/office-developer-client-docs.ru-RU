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
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808830"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Относится к**: Outlook 
  
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

