---
title: Ипропдатахрсетобжакцесс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425157"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает уровень доступа для объекта.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Параметры

 _Улакцесс_
  
> возврата Битовая маска флагов, определяющая уровень доступа объекта. Можно задать один из следующих флагов:
    
ИПРОП_РЕАДОНЛИ 
  
> Задает уровень доступа для объекта "только для чтения". 
    
ИПРОП_РЕАДВРИТЕ 
  
> Задает уровень доступа объекта для чтения и записи.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уровень доступа объекта успешно установлен.
    
## <a name="remarks"></a>Примечания

Метод **ипропдата:: хрсетобжакцесс** устанавливает уровень доступа для всего объекта, а не для отдельных свойств. **Хрсетобжакцесс** можно использовать для изменения уровня доступа, установленного при создании объекта. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы задать уровень доступа к свойству, сначала необходимо вызвать **хрсетобжакцесс** с ФЛАГом ипроп_реадврите, установленным в параметре _улакцесс_ , чтобы сделать объект изменяемым. Затем вызовите метод [ипропдата:: хрсетпропакцесс](ipropdata-hrsetpropaccess.md) , указав свойство Target в массиве, на которое указывает параметр _лппроптагаррай_ . 
  
Чтобы создать объект со свойствами, которые будут доступны только для чтения, создайте объект для чтения и записи, добавьте необходимые свойства, а затем вызовите **хрсетобжакцесс** , чтобы изменить доступ объекта только для чтения. 
  
Кроме того, вы можете использовать **хрсетобжакцесс** , чтобы запретить клиентам создавать новые свойства. 
  
## <a name="see-also"></a>См. также



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

