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
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809524"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Относится к**: Outlook 
  
Предоставляет возможность извлекать и изменять уровень доступа для свойств объекта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Предоставляемые:  <br/> |Объект данных свойств  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщиков услуг и клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIPropData  <br/> |
|Тип указателя:  <br/> |LPPROPDATA  <br/> |
|Модель транзакций:  <br/> |Не входящих в транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Задает уровень доступа для объекта.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Задает уровень доступа и состояние для одной или нескольких свойств объекта.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Получает уровень доступа и состояние для одной или нескольких свойств объекта.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Добавление одного или нескольких свойств типа PT_OBJECT объект.  <br/> |
   
## <a name="remarks"></a>Замечания

Интерфейс **IPropData::IMAPIProp** реализован MAPI и используется в первую очередь поставщиками услуг, обращающихся к этой реализации путем вызова функции [CreateIProp](createiprop.md) . 
  
Дополнительные сведения о уровни доступа для объектов и свойств содержатся в разделе [разрешения для объектов и свойств](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

