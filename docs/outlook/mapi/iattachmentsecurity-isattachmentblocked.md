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
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565048"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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



[Константы MAPI](mapi-constants.md)
  
[Убедитесь, что Заблокированные вложения](how-to-verify-an-attachment-is-blocked.md)

