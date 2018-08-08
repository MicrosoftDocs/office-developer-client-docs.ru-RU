---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808813"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Относится к**: Outlook 
  
Получает сведения о поддержке папки для совместного доступа.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Параметры

 _pdwSupportMask_
  
> [out] Битовая маска, указывающее, поддерживает ли общий доступ к папке.
    
 **FS_NONE**
  
> Указывает, что папка не поддерживает общий доступ.
    
 **FS_SUPPORTS_SHARING**
  
> Указывает, что папка поддерживает общий доступ.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов выполнен успешно.
    

