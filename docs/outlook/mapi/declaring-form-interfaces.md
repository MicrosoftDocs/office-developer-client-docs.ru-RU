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
ms.openlocfilehash: 8f4d8842efbba2f1f2b7281e5d4741b89f975b3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808257"
---
# <a name="declaring-form-interfaces"></a>Объявление интерфейсов форм

  
  
**Относится к**: Outlook 
  
Объявления реализации интерфейсов формы MAPI можно упростить с помощью макросов _interface__METHOD MAPI_, где _интерфейс_ является интерфейсом формы, определенные в файле заголовка Mapiform.h. С помощью этих макросов не требуется, но если вы не должен выполнять внимание соответствия объявлениях объявления в файл заголовка Mapiform.h. Например можно объявить класс объекта формы сервера форм следующим образом: 
  
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



[Написание серверного кода формы](writing-form-server-code.md)

