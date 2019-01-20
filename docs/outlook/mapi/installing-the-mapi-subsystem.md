---
title: Установка подсистемы MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Дата последнего изменения: 9 марта 2015 г.'
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722440"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="6ae4a-103">Установка подсистемы MAPI</span><span class="sxs-lookup"><span data-stu-id="6ae4a-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="6ae4a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ae4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ae4a-105">Поддерживаемые версии Windows устанавливают библиотеки-заглушки MAPI (Mapi32.dll) в папку _\<ИмяДиска\>_ \Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="6ae4a-106">Ниже перечислены поддерживаемые версии Windows.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="6ae4a-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-107">Windows 7</span></span>
    
- <span data-ttu-id="6ae4a-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-108">Windows Vista</span></span>
    
- <span data-ttu-id="6ae4a-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-109">Windows Server 2008</span></span>
    
- <span data-ttu-id="6ae4a-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-110">Windows Server 2003</span></span>
    
- <span data-ttu-id="6ae4a-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-111">Windows XP</span></span>
    
<span data-ttu-id="6ae4a-112">Чтобы правильно установить подсистему MAPI, установите приложение, которое содержит подсистему на основе MAPI, например Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="6ae4a-113">Сведения об установленной подсистеме MAPI компьютера см. в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="6ae4a-114">Все значения в записях реестра представляют собой строки символов.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="6ae4a-115">Программы установки служб обмена сообщениями отвечают за создание сведений об установке в следующем разделе системного реестра:</span><span class="sxs-lookup"><span data-stu-id="6ae4a-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="6ae4a-116">Службы обмена сообщениями должны добавлять записи в системный реестр.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="6ae4a-117">В таблице ниже содержится информация о том, как клиенты получают сведения о версии для подсистемы MAPI на своих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="6ae4a-118">**Сведения, которые необходимо проверить**</span><span class="sxs-lookup"><span data-stu-id="6ae4a-118">**To check**</span></span>|<span data-ttu-id="6ae4a-119">**Реестр**</span><span class="sxs-lookup"><span data-stu-id="6ae4a-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ae4a-120">Доступность MAPI</span><span class="sxs-lookup"><span data-stu-id="6ae4a-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="6ae4a-121">Найдите раздел реестра `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="6ae4a-122">Доступная версия MAPI</span><span class="sxs-lookup"><span data-stu-id="6ae4a-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="6ae4a-123">Найдите строку MAPIXVER вида _x.x.x_.</span><span class="sxs-lookup"><span data-stu-id="6ae4a-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ae4a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6ae4a-124">See also</span></span>



[<span data-ttu-id="6ae4a-125">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="6ae4a-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

