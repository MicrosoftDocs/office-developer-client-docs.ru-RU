---
title: Имапиформинфомакеиконфромбинари
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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342114"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает значок на основе одного из свойств значка формы.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Параметры

 _Нпропид_
  
> возврата Идентификатор свойства для свойства Icon.
    
 _фикон_
  
> вышли Указатель на возвращаемый значок.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Комментарии

Клиентские приложения вызывают метод **имапиформинфо:: макеиконфромбинари** для создания значка из одного из свойств значков формы. В параметре _Нпропид_ **макеиконфромбинари** принимает идентификатор свойства одного из свойств Icon формы. При использовании этого идентификатора свойства создается значок, который может отображаться в представлениях таблицы, включающих в себя столбцы свойств для значков. 
  
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

