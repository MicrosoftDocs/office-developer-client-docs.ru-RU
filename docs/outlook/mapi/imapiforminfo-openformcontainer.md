---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 16e1d45806755bad8caff6847b0ecdea5b4ba78b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590423"
---
# <a name="imapiforminfoopenformcontainer"></a>IMAPIFormInfo::OpenFormContainer

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на контейнер формы, в которой установлен определенной формы.
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a>Параметры

 _ppformcontainer_
  
> [out] Указатель на указатель на объект контейнера возвращенные формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

