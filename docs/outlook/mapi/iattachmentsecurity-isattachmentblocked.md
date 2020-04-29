---
title: иаттачментсекуритисаттачментблоккед
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
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439781"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет, блокируется ли указанное вложение приложением Microsoft Outlook 2010 или Microsoft Outlook 2013 для просмотра и индексирования.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Параметры

 _пвсзфиленаме_
  
> возврата Указатель на имя файла вложения.
    
 _пфблоккед_
  
> вышли Указатель на значение **true** , если указанное вложение заблокировано; в противном случае — **false**.
    
## <a name="see-also"></a>См. также



[Константы MAPI](mapi-constants.md)
  
[Проверка блокировки вложения](how-to-verify-an-attachment-is-blocked.md)

