---
title: Объявление интерфейсов форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437513"
---
# <a name="declaring-form-interfaces"></a>Объявление интерфейсов форм

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Вы можете упростить объявления реализации интерфейсов форм MAPI с помощью MAPI_ макросов _interface__METHOD, где _Interface_ — это интерфейс формы, определенный в файле заголовка мапиформ. h. Вы не обязаны использовать эти макросы, но если это не так, следует принять определенные меры, которые соответствуют объявлениям в файле заголовка Мапиформ. h. Например, можно объявить класс объекта формы сервера форм, как показано ниже: 
  
```cpp
class CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructorr takes a class factory object
    ~CMyForm(void);
// MAPI methods that need to be implemented.
    MAPI_IUNKNOWN_METHODS(IMPL);
    MAPI_GETLASTERROR_METHOD(IMPL);
    MAPI_IPERSISTMESSAGE_METHODS(IMPL);
    MAPI_IMAPIFORM_METHODS(IMPL);
    MAPI_IMAPIFORMADVISESINK_METHODS(IMPL);
// Add other implementation specific items.
};

```

## <a name="see-also"></a>См. также



[Написание кода на сервере формы](writing-form-server-code.md)

