---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435147"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет возможность получения и изменения доступа для свойств объекта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Подвергается:  <br/> |Объект данных свойства  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг и клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIPropData  <br/> |
|Тип указателя:  <br/> |LPPROPDATA  <br/> |
|Модель транзакции:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Задает уровень доступа для объекта.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Задает уровень и состояние доступа для одного или более свойств объекта.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Извлекает уровень и состояние доступа для одного или более свойств объекта.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Добавляет одно или несколько свойств типа PT_OBJECT объекту.  <br/> |
   
## <a name="remarks"></a>Примечания

Интерфейс **IPropData::IMAPIProp** реализуется MAPI и используется в основном поставщиками услуг, которые используют эту реализацию, вызывая функцию [CreateIProp.](createiprop.md) 
  
Дополнительные сведения об уровнях доступа к объектам и свойствам см. в дополнительных сведениях [о разрешениях для объектов и свойств.](permissions-for-mapi-objects-and-properties.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

