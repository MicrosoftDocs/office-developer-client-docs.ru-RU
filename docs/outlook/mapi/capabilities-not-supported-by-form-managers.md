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
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419382"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="0802b-103">Возможности, не поддерживаемые диспетчерами форм</span><span class="sxs-lookup"><span data-stu-id="0802b-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="0802b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0802b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0802b-105">Следующие функции не поддерживаются менеджером форм по умолчанию из соображений производительности, но могут быть поддержаны настраиваемые менеджеры форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="0802b-106">Иерархия, которая позволяет сгруппированы или классифицируются формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="0802b-107">Библиотека форм — это база данных форм с плоским файлом.</span><span class="sxs-lookup"><span data-stu-id="0802b-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="0802b-108">Управление доступом для категорий форм, соответствующих классам сообщений или суперклассам.</span><span class="sxs-lookup"><span data-stu-id="0802b-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="0802b-109">Поддержка нескольких языковых версий одной формы в одной библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="0802b-110">Это проблемы реализации.</span><span class="sxs-lookup"><span data-stu-id="0802b-110">These are implementation issues.</span></span> <span data-ttu-id="0802b-111">Нет ничего, чтобы предотвратить реализацию этих функций настраиваемой диспетчером форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="0802b-112">Архитектура форм MAPI не поддерживает одновременное управление несколькими руководителями форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="0802b-113">Хотя MAPI поддерживает несколько одновременно поставщиков, поставщиков транспортных сообщений и поставщиков адресных книг, поддерживается только один диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="0802b-114">Так как одновременно может выполняться только один диспетчер форм, если вы реализуете настраиваемый диспетчер форм, вам придется повторно реализовать все функции из нужного по умолчанию администратора форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="0802b-115">Так как настраиваемый диспетчер форм полностью заменит диспетчер форм по умолчанию, возможности диспетчера форм по умолчанию будут недоступны, если они не будут дублироваться в настраиваемом диспетчере форм.</span><span class="sxs-lookup"><span data-stu-id="0802b-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0802b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="0802b-116">See also</span></span>



[<span data-ttu-id="0802b-117">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="0802b-117">MAPI Forms</span></span>](mapi-forms.md)

