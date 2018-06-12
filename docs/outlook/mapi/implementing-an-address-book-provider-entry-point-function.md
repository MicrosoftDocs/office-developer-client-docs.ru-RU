---
title: Реализация функцию адресной книги поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809301"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="982a3-103">Реализация функцию адресной книги поставщика</span><span class="sxs-lookup"><span data-stu-id="982a3-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="982a3-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="982a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="982a3-105">При клиентского приложения вызовы [MAPILogonEx](mapilogonex.md) для начала сеанса с использованием профиля, содержащего адресной книге, MAPI загружает поставщика и все остальные, которые являются частью профиля.</span><span class="sxs-lookup"><span data-stu-id="982a3-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="982a3-106">Имя функции точки входа вашего поставщика анализирует MAPI, изучив в профиле.</span><span class="sxs-lookup"><span data-stu-id="982a3-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="982a3-107">Помните, что эта функция не то же, что функция точки входа DLL; Обратитесь к документации по **DllMain** в документации по Win32.</span><span class="sxs-lookup"><span data-stu-id="982a3-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="982a3-108">Существует несколько записей, некоторые из них, которые должны встречаться в файле конфигурации mapisvc.inf, включенные в разделе профиль каждый поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="982a3-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="982a3-109">В следующей таблице перечислены эти записи раздела профиля и того, является ли их необходимо включить файла mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="982a3-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="982a3-110">**Запись раздела профиля**</span><span class="sxs-lookup"><span data-stu-id="982a3-110">**Profile section entry**</span></span>|<span data-ttu-id="982a3-111">**требование Mapisvc.inf**</span><span class="sxs-lookup"><span data-stu-id="982a3-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="982a3-112">PR_DISPLAY_NAME = _строка_</span><span class="sxs-lookup"><span data-stu-id="982a3-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="982a3-113">Optional</span><span class="sxs-lookup"><span data-stu-id="982a3-113">Optional</span></span>  <br/> |
|<span data-ttu-id="982a3-114">PR_PROVIDER_DISPLAY = _строка_</span><span class="sxs-lookup"><span data-stu-id="982a3-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="982a3-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="982a3-115">Required</span></span>  <br/> |
|<span data-ttu-id="982a3-116">PR_PROVIDER_DLL_NAME = _имя DLL-файла_</span><span class="sxs-lookup"><span data-stu-id="982a3-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="982a3-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="982a3-117">Required</span></span>  <br/> |
|<span data-ttu-id="982a3-118">PR_RESOURCE_TYPE = _длинный_</span><span class="sxs-lookup"><span data-stu-id="982a3-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="982a3-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="982a3-119">Required</span></span>  <br/> |
|<span data-ttu-id="982a3-120">PR_RESOURCE_FLAGS = _битовой маски_</span><span class="sxs-lookup"><span data-stu-id="982a3-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="982a3-121">Optional</span><span class="sxs-lookup"><span data-stu-id="982a3-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="982a3-122">Поставщик адресной книги можно поместить эти сведения в профиль непосредственно путем вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля или косвенно, изменяя MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="982a3-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="982a3-123">Профили создаются с помощью информацию в файл Mapisvc.inf. INF для выбранных поставщиков или службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="982a3-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="982a3-124">Дополнительные сведения об организации и содержимое файл Mapisvc.inf. INF, просмотрите [Файл формата MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="982a3-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="982a3-125">Имя функции точки входа DLL вашей адресной книге должно быть [ABProviderInit](abproviderinit.md) , и он должен соответствовать типу прототип **ABProviderInit** .</span><span class="sxs-lookup"><span data-stu-id="982a3-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="982a3-126">В ваш поставщик функцию точки входа DLL выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="982a3-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="982a3-127">Проверка версии интерфейс поставщика службы (SPI), чтобы убедиться в том, что используется версия, совместимый с версией, которая использует ваш поставщик адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="982a3-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="982a3-128">Создайте экземпляр объекта поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="982a3-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="982a3-129">Не вызывайте **MAPIInitialize** или **MAPIUninitialize** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="982a3-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="982a3-130">Функции точки входа DLL создает экземпляр объекта поставщика и возвращает указатель на этот объект MAPI.</span><span class="sxs-lookup"><span data-stu-id="982a3-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

