---
title: Ипропдата IMAPIProp
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279544"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет возможность извлечения и изменения доступа к свойствам объекта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Предоставлено:  <br/> |Объект данных свойства  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг и клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапипропдата  <br/> |
|Тип указателя:  <br/> |ЛППРОПДАТА  <br/> |
|Модель транзакции:  <br/> |Не transactd  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Хрсетобжакцесс](ipropdata-hrsetobjaccess.md) <br/> |Задает уровень доступа для объекта.  <br/> |
|[Хрсетпропакцесс](ipropdata-hrsetpropaccess.md) <br/> |Задает уровень доступа и состояние для одного или нескольких свойств объекта.  <br/> |
|[Хржетпропакцесс](ipropdata-hrgetpropaccess.md) <br/> |Получает уровень доступа и состояние для одного или нескольких свойств объекта.  <br/> |
|[Храддобжпропс](ipropdata-hraddobjprops.md) <br/> |Добавляет одно или несколько свойств типа ПТ_ОБЖЕКТ в объект.  <br/> |
   
## <a name="remarks"></a>Замечания

Интерфейс **ипропдата:: IMAPIProp** реализуется MAPI и используется преимущественно поставщиками услуг, которые обращаются к этой реализации, вызывая функцию [креатеипроп](createiprop.md) . 
  
Дополнительные сведения о уровнях доступа к объектам и свойствам содержатся в разделе [разрешения для объектов и свойств](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

