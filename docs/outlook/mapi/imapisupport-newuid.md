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
ms.openlocfilehash: 244087c41e33e470c42434e9d57cee7317bcb78c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571691"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает новую структуру [MAPIUID](mapiuid.md) для использования в качестве уникального идентификатора. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Параметры

 _lpMuid_
  
> Указатель на структуру нового **MAPIUID** . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Был создан новый структуры **MAPIUID** . 
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::NewUID** применяется для всех объектов поддержки. Поставщики службы и службы сообщений вызов **NewUID** каждый раз, когда они должны получать долгосрочного уникального идентификатора. Сообщение хранилища поставщика, например, можно вызвать метод **NewUID** для получения **MAPIUID** для помещения в свойство **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) только что созданный сообщения.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не следует путать структуру **MAPIUID** , зарегистрируйте во время входа в систему с помощью структуры **MAPIUID** , метод **NewUID** создает. Структура **MAPIUID** , зарегистрируйте при вызове метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) представляет адресной книги или сообщение хранения поставщика MAPI и используется для различения идентификаторы записей, создаваемых различных поставщиков. Эта структура **MAPIUID** следует жестко и не получить путем вызова **NewUID**.
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

