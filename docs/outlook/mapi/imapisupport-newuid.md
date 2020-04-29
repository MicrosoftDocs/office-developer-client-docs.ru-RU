---
title: имаписуппортневуид
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
  
Создает новую структуру [мапиуид](mapiuid.md) , которая будет использоваться в качестве уникального идентификатора. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Параметры

 _лпмуид_
  
> Указатель на новую структуру **мапиуид** . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Создана новая структура **мапиуид** . 
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: невуид** реализован для всех объектов поддержки. Поставщики услуг и службы сообщений вызывайте **невуид** , когда им нужно создать долгосрочный уникальный идентификатор. Поставщик хранилища сообщений, например, может вызывать **невуид** для получения **мапиуид** , помещаемого в свойство **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) только что созданного сообщения.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не путайте структуру **мапиуид** , которую вы регистрируете во время входа в структуры **мапиуид** , создаваемые методом **невуид** . Структура **мапиуид** , регистрируемая при вызове метода [Имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) , представляет адресную книгу или поставщика хранилища сообщений для MAPI и используется для различения идентификаторов записей, создаваемых различными поставщиками. Эта структура **мапиуид** должна быть жестко запрограммирована и не была получена через вызов **невуид**.
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

