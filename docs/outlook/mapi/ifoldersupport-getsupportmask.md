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
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417373"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает сведения о поддержке папки для общего доступа.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Параметры

 _pdwSupportMask_
  
> [out] Битоваяmas, указывающая, поддерживает ли папка общий доступ.
    
 **FS_NONE**
  
> Указывает, что папка не поддерживает общий доступ.
    
 **FS_SUPPORTS_SHARING**
  
> Указывает, что папка поддерживает общий доступ.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным.
    

