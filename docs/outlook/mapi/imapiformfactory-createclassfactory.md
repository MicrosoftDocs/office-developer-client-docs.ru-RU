---
title: имапиформфакторикреатеклассфактори
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416078"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="8c631-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="8c631-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="8c631-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c631-105">Возвращает объект фабрики класса для формы.</span><span class="sxs-lookup"><span data-stu-id="8c631-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="8c631-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c631-106">Parameters</span></span>

 <span data-ttu-id="8c631-107">_клсидформ_</span><span class="sxs-lookup"><span data-stu-id="8c631-107">_clsidForm_</span></span>
  
> <span data-ttu-id="8c631-108">возврата Идентификатор класса для формы, создаваемой фабрикой классов.</span><span class="sxs-lookup"><span data-stu-id="8c631-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="8c631-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8c631-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8c631-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="8c631-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8c631-111">_лппклассфактори_</span><span class="sxs-lookup"><span data-stu-id="8c631-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="8c631-112">вышли Указатель на объект фабрики класса.</span><span class="sxs-lookup"><span data-stu-id="8c631-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8c631-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c631-113">Return value</span></span>

<span data-ttu-id="8c631-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c631-114">S_OK</span></span> 
  
> <span data-ttu-id="8c631-115">Был возвращен объект фабрики класса.</span><span class="sxs-lookup"><span data-stu-id="8c631-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c631-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c631-116">Remarks</span></span>

<span data-ttu-id="8c631-117">Средства просмотра форм вызывают метод **имапиформфактори:: креатеклассфактори** для получения фабрики класса для определенной формы.</span><span class="sxs-lookup"><span data-stu-id="8c631-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="8c631-118">Фабрика классов используется для создания экземпляров формы, которые обрабатывают сообщения определенного класса и контролируют доступ к этим экземплярам.</span><span class="sxs-lookup"><span data-stu-id="8c631-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="8c631-119">Метод **креатеклассфактори** вызывается средствами просмотра формы для получения объекта фабрики класса для серверов форм, которые реализуют несколько классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="8c631-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="8c631-120">Этот метод получает идентификатор класса (CLSID) в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="8c631-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="8c631-121">В зависимости от этого параметра этот метод может определить конкретный вид объекта фабрики класса, который требуется возвратить.</span><span class="sxs-lookup"><span data-stu-id="8c631-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8c631-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8c631-122">Notes to implementers</span></span>

<span data-ttu-id="8c631-123">Вы можете вернуться от реализации **креатеклассфактори** к тому же объекту фабрики класса для нескольких вызовов для одного и того же идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="8c631-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="8c631-124">Создание нового экземпляра фабрики классов не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8c631-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="8c631-125">Вы можете реализовать фабрику одного класса, которая создает соответствующие экземпляры фабрики классов по запросу или несколько реализаций фабрики классов, по одному для каждого класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="8c631-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c631-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8c631-126">See also</span></span>



[<span data-ttu-id="8c631-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c631-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

