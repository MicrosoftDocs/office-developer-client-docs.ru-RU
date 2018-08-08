---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 45e4362fc025c1784e9432c5d641e865a044bd00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808788"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Относится к**: Outlook 
  
Проверяет, если указанное вложение не заблокирован по Microsoft Outlook 2010 или Microsoft Outlook 2013 для просмотра и индексирования.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Параметры

 _pwszFileName_
  
> [in] Указатель на имени файла вложения.
    
 _pfBlocked_
  
> [out] Указатель на значение, указывающее **значение true,** Если указанное вложение блокируется. в противном случае — **false**.
    
## <a name="see-also"></a>См. также



[��������� MAPI](mapi-constants.md)
  
[Проверка блокировки вложения](how-to-verify-an-attachment-is-blocked.md)

