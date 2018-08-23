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
ms.openlocfilehash: 4687b07c89d866acbe3b6a8f4cde3262657a06b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584249"
---
# <a name="declaring-form-interfaces"></a><span data-ttu-id="39d5e-103">Объявление интерфейсов форм</span><span class="sxs-lookup"><span data-stu-id="39d5e-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="39d5e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39d5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39d5e-105">Объявления реализации интерфейсов формы MAPI можно упростить с помощью макросов _interface__METHOD MAPI_, где _интерфейс_ является интерфейсом формы, определенные в файле заголовка Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="39d5e-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="39d5e-106">С помощью этих макросов не требуется, но если вы не должен выполнять внимание соответствия объявлениях объявления в файл заголовка Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="39d5e-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="39d5e-107">Например можно объявить класс объекта формы сервера форм следующим образом:</span><span class="sxs-lookup"><span data-stu-id="39d5e-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="39d5e-108">См. также</span><span class="sxs-lookup"><span data-stu-id="39d5e-108">See also</span></span>



[<span data-ttu-id="39d5e-109">Написание серверного кода формы</span><span class="sxs-lookup"><span data-stu-id="39d5e-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

