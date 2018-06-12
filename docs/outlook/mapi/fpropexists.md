---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808500"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Применимо к**: Outlook 
  
Выполняет поиск тега заданного свойства в интерфейс [IMAPIProp](imapipropiunknown.md) или интерфейса на основе **IMAPIProp**, такие как [IMessage](imessageimapiprop.md) или [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameters

 _pobj_
  
> [in] Указатель на интерфейс **IMAPIProp** или интерфейс, производные от **IMAPIProp** , в которой нужно выполнить поиск тега свойства. 
    
 _ulPropTag_
  
> [in] Свойство tag для поиска.
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Найдено совпадение для тега данного свойства. 
    
FALSE 
  
> Не найдено соответствие для указанного свойства тега.
    
## <a name="remarks"></a>Замечания

Если свойство tag с помощью параметра _ulPropTag_ имеет тип PT_UNSPECIFIED, функция **FPropExists** выполняет поиск только на основе свойства идентификатора соответствия. В противном случае учитывается для тега всего свойства, включая тип. 
  

