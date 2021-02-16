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
# <a name="declaring-form-interfaces"></a><span data-ttu-id="6e29a-103">Объявление интерфейсов форм</span><span class="sxs-lookup"><span data-stu-id="6e29a-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="6e29a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e29a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e29a-105">Можно упростить объявления реализации интерфейсов форм MAPI с помощью макроса MAPI_ _interface__METHOD,  где интерфейс — это интерфейс формы, определенный в файле загона Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="6e29a-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="6e29a-106">Использовать эти макрос не обязательно, но в этом случае следует соблюдать объявления в файле загона Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="6e29a-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="6e29a-107">Например, можно объявить класс объекта формы сервера форм следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6e29a-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="6e29a-108">См. также</span><span class="sxs-lookup"><span data-stu-id="6e29a-108">See also</span></span>



[<span data-ttu-id="6e29a-109">Написание кода сервера форм</span><span class="sxs-lookup"><span data-stu-id="6e29a-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

