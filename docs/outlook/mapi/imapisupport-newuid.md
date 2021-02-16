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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает новую структуру [MAPIUID,](mapiuid.md) которая будет использоваться в качестве уникального идентификатора. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Параметры

 _lpMuid_
  
> Указатель на новую структуру **MAPIUID.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Создана новая **структура MAPIUID.** 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::NewUID** реализован для всех объектов поддержки. Поставщики услуг и службы сообщений вызывают **NewUID** всякий раз, когда им нужно создать долгосрочный уникальный идентификатор. Например, поставщик store сообщений может вызвать **NewUID,** чтобы получить **MAPIUID,** чтобы поместить его в свойство **PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)только что созданного сообщения.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не путайте **структуру MAPIUID,** зарегистрированную во время регистрации, со структурами **MAPIUID,** которые создает метод **NewUID.** Структура **MAPIUID,** которую вы регистрируете при вызове метода [IMAPISupport::SetProviderUID,](imapisupport-setprovideruid.md) представляет вашу адресную книгу или поставщика магазина сообщений mapI и используется для различия идентификаторов записей, которые создают разные поставщики. Эта **структура MAPIUID** должна быть жестко заданной и не может быть получена при вызове **NewUID.**
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

