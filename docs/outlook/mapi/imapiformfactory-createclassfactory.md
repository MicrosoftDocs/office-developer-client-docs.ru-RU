---
title: IMAPIFormFactoryCreateClassFactory
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
ms.openlocfilehash: cb5cb5a0169e716f7fcc7f596660bc0222c51c84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572160"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="11b14-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="11b14-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="11b14-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11b14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11b14-105">Возвращает объект фабрики класса для формы.</span><span class="sxs-lookup"><span data-stu-id="11b14-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="11b14-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11b14-106">Parameters</span></span>

 <span data-ttu-id="11b14-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="11b14-107">_clsidForm_</span></span>
  
> <span data-ttu-id="11b14-108">[in] Идентификатор класса для формы будет создан с помощью класса.</span><span class="sxs-lookup"><span data-stu-id="11b14-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="11b14-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11b14-109">_ulFlags_</span></span>
  
> <span data-ttu-id="11b14-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="11b14-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="11b14-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="11b14-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="11b14-112">[out] Указатель на объект фабрики класса.</span><span class="sxs-lookup"><span data-stu-id="11b14-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11b14-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="11b14-113">Return value</span></span>

<span data-ttu-id="11b14-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="11b14-114">S_OK</span></span> 
  
> <span data-ttu-id="11b14-115">Возвращает объект фабрики класса.</span><span class="sxs-lookup"><span data-stu-id="11b14-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11b14-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="11b14-116">Remarks</span></span>

<span data-ttu-id="11b14-117">Средства просмотра форм вызовите метод **IMAPIFormFactory::CreateClassFactory** для получения фабрики классов для определенной формы.</span><span class="sxs-lookup"><span data-stu-id="11b14-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="11b14-118">Фабрика классов используется для создания экземпляров формы, которая обрабатывает сообщения определенного класса и для управления доступом к эти экземпляры.</span><span class="sxs-lookup"><span data-stu-id="11b14-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="11b14-119">Метод **CreateClassFactory** вызывается средства просмотра формы для получения объекта фабрики класса для серверов форм, которые реализуют несколько классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="11b14-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="11b14-120">Этот метод получает идентификатор класса (CLSID) как параметр.</span><span class="sxs-lookup"><span data-stu-id="11b14-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="11b14-121">На основе этого параметра, этот метод можно определить определенного вида объекта фабрики класса для возврата.</span><span class="sxs-lookup"><span data-stu-id="11b14-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="11b14-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="11b14-122">Notes to implementers</span></span>

<span data-ttu-id="11b14-123">Можно вернуть от внедрения **CreateClassFactory** один и тот же объект фабрики класса на несколько вызовов для один и тот же идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="11b14-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="11b14-124">Создание нового экземпляра класса фабрики не требуется.</span><span class="sxs-lookup"><span data-stu-id="11b14-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="11b14-125">Может иметь реализацию фабрики одного класса, который создает экземпляры фабрики соответствующий класс по запросу или нескольких реализации фабрики классов, другая — для каждого класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="11b14-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11b14-126">См. также</span><span class="sxs-lookup"><span data-stu-id="11b14-126">See also</span></span>



[<span data-ttu-id="11b14-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11b14-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

