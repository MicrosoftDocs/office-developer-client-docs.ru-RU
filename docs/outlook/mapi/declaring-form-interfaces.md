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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вы можете упростить объявления о реализации интерфейсов форм MAPI с помощью макрос MAPI_ _interface__METHOD, где интерфейс — это интерфейс формы, определенный в заглавном файле Mapiform.h.  Вы не обязаны использовать эти макрос, но если вы этого не сделаете, следует особо заботиться о том, чтобы ваши декларации соответствовали декларациям в файле загона Mapiform.h. Например, можно объявить класс объекта формы сервера формы следующим образом: 
  
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



[Написание кода сервера форм](writing-form-server-code.md)

