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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337060"
---
# <a name="declaring-form-interfaces"></a><span data-ttu-id="15397-103">Объявление интерфейсов форм</span><span class="sxs-lookup"><span data-stu-id="15397-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="15397-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15397-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15397-105">Вы можете упростить объявления реализации интерфейсов форм MAPI с помощью макросов МАПИ_ _Интерфаце__месод, где _Interface_ — это интерфейс формы, определенный в файле заголовка мапиформ. h.</span><span class="sxs-lookup"><span data-stu-id="15397-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="15397-106">Вы не обязаны использовать эти макросы, но если это не так, следует принять определенные меры, которые соответствуют объявлениям в файле заголовка Мапиформ. h.</span><span class="sxs-lookup"><span data-stu-id="15397-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="15397-107">Например, можно объявить класс объекта формы сервера форм, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="15397-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="15397-108">См. также</span><span class="sxs-lookup"><span data-stu-id="15397-108">See also</span></span>



[<span data-ttu-id="15397-109">Написание кода на сервере формы</span><span class="sxs-lookup"><span data-stu-id="15397-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

