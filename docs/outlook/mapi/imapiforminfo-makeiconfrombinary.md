---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570130"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает значок из одного из свойств значок формы.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Параметры

 _nPropID_
  
> [in] Идентификатор свойства для значка свойства.
    
 _phicon_
  
> [out] Указатель на возвращаемый значок.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Клиентские приложения вызовите метод **IMAPIFormInfo::MakeIconFromBinary** для создания значка из одного из свойств значок формы. В параметре _nPropID_ **MakeIconFromBinary** принимает идентификатор свойства одного из свойств значок формы. Использование этого свойства идентификатора, построение выполнено значок, который может отображаться в табличном представлении, включая столбцы свойств для значков. 
  
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

