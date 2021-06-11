---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406999"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает новую [структуру MAPIUID,](mapiuid.md) которая будет использоваться в качестве уникального идентификатора. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parameters

 _lpMuid_
  
> Указатель на новую **структуру MAPIUID.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Была создана **новая структура MAPIUID.** 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::NewUID** реализован для всех объектов поддержки. Поставщики услуг и службы сообщений вызывают **NewUID** всякий раз, когда им необходимо создать долгосрочный уникальный идентификатор. Например, поставщик магазина сообщений может вызвать **NewUID** для получения **MAPIUID** для вложения **в свойство** [PR_SEARCH_KEY (PidTagSearchKey)](pidtagsearchkey-canonical-property.md)вновь созданного сообщения.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не путайте **структуру MAPIUID,** которую вы регистрируете во время регистрации, со структурами **MAPIUID,** которые создает метод **NewUID.** Структура **MAPIUID,** которую вы регистрируете при вызове метода [IMAPISupport::SetProviderUID,](imapisupport-setprovideruid.md) представляет вашу адресную книгу или поставщика магазина сообщений в MAPI и используется для различия идентификаторов записей, которые создают различные поставщики. Эта **структура MAPIUID** должна быть жестко закодироваться и не получена при вызове **в NewUID.**
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

