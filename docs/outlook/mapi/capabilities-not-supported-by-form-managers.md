---
title: Возможности, не поддерживаемые диспетчерами форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86c91353b620482ca0862aa998aae1b3329cfc94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808125"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="86b4e-103">Возможности, не поддерживаемые диспетчерами форм</span><span class="sxs-lookup"><span data-stu-id="86b4e-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="86b4e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86b4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86b4e-105">Следующие функции не поддерживаются диспетчером формы по умолчанию в целях повышения производительности, но могут поддерживаться руководителями настраиваемой формы.</span><span class="sxs-lookup"><span data-stu-id="86b4e-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="86b4e-106">Иерархия, которая позволяет форм для группировки или по категориям во всей библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="86b4e-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="86b4e-107">Библиотеки форм представляет собой файл базу данных из форм.</span><span class="sxs-lookup"><span data-stu-id="86b4e-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="86b4e-108">Управление доступом для категорий форм, соответствующий классы сообщений или суперклассов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="86b4e-109">Поддержка различных языковых версий этой же формы в библиотеке одной формы.</span><span class="sxs-lookup"><span data-stu-id="86b4e-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="86b4e-110">Далее представлены проблемы реализации.</span><span class="sxs-lookup"><span data-stu-id="86b4e-110">These are implementation issues.</span></span> <span data-ttu-id="86b4e-111">Не требуется запретить Диспетчер настраиваемой формы реализации этих функций.</span><span class="sxs-lookup"><span data-stu-id="86b4e-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="86b4e-112">Архитектура формы MAPI не поддерживает несколько диспетчеров формы, выполняемых одновременно.</span><span class="sxs-lookup"><span data-stu-id="86b4e-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="86b4e-113">Хотя MAPI поддерживает несколько поставщиков хранилища параллельных сообщения, поставщиками транспорта и поставщиками адресных книг, поддерживается только диспетчер одной формы.</span><span class="sxs-lookup"><span data-stu-id="86b4e-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="86b4e-114">Так как диспетчер только одна форма может выполняться за один раз при реализации диспетчера настраиваемой формы необходимо повторно реализовать функциональные возможности от руководителя формы по умолчанию, который требуется.</span><span class="sxs-lookup"><span data-stu-id="86b4e-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="86b4e-115">Так как диспетчеру настраиваемой формы будет полностью заменить диспетчер форм по умолчанию, возможности диспетчера формы по умолчанию будет недоступен, пока они дублируются в ваш начальник настраиваемой формы.</span><span class="sxs-lookup"><span data-stu-id="86b4e-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86b4e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="86b4e-116">See also</span></span>



[<span data-ttu-id="86b4e-117">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="86b4e-117">MAPI Forms</span></span>](mapi-forms.md)

