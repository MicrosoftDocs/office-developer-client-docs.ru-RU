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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405116"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает значок из одного из свойств значка формы.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Параметры

 _nPropID_
  
> [in] Идентификатор свойства для свойства значка.
    
 _phicon_
  
> [out] Указатель на возвращенный значок.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызывать метод **IMAPIFormInfo::MakeIconFromBinary,** чтобы создать значок из одного из свойств значка формы. В  _параметре nPropID_ **MakeIconFromBinary** принимает идентификатор свойства одного из свойств значка формы. С помощью этого идентификатора свойства он создает значок, который может отображаться в представлениях таблиц, включая столбцы свойств для значков. 
  
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

