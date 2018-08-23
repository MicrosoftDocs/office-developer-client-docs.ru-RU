---
title: Установка подсистемы MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: adb4d09ccce95683ac46e7b271fafa328b1a9f97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575352"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="fc89f-103">Установка подсистемы MAPI</span><span class="sxs-lookup"><span data-stu-id="fc89f-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="fc89f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc89f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc89f-105">Поддерживаемые версии Windows Установка библиотеки заглушка MAPI, Mapi32.dll, в _ \<диск\>_ \Windows\System32 папки.</span><span class="sxs-lookup"><span data-stu-id="fc89f-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="fc89f-106">Поддерживаемые версии Windows, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="fc89f-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="fc89f-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc89f-107">Windows 7.</span></span>
    
- <span data-ttu-id="fc89f-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc89f-108">Windows Vista.</span></span>
    
- <span data-ttu-id="fc89f-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fc89f-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="fc89f-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fc89f-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="fc89f-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc89f-111">Windows XP.</span></span>
    
<span data-ttu-id="fc89f-112">Для правильной установки подсистемы MAPI установите приложения, содержащего подсистемы на основе MAPI, например Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="fc89f-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="fc89f-113">Сведения об установке подсистемы MAPI компьютера можно найти в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="fc89f-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="fc89f-114">Все значения в записях реестра: строк символов.</span><span class="sxs-lookup"><span data-stu-id="fc89f-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="fc89f-115">Программы установки службы сообщений отвечают за создание сведения об установке в следующий раздел реестра системы:</span><span class="sxs-lookup"><span data-stu-id="fc89f-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="fc89f-116">Службы сообщений необходимо добавить записей системного реестра.</span><span class="sxs-lookup"><span data-stu-id="fc89f-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="fc89f-117">В следующей таблице представлены как клиенты получить сведения о версии подсистемы MAPI на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="fc89f-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="fc89f-118">**Для проверки**</span><span class="sxs-lookup"><span data-stu-id="fc89f-118">**To check**</span></span>|<span data-ttu-id="fc89f-119">**Реестра**</span><span class="sxs-lookup"><span data-stu-id="fc89f-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc89f-120">Доступность MAPI</span><span class="sxs-lookup"><span data-stu-id="fc89f-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="fc89f-121">Найдите `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="fc89f-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="fc89f-122">Доступная версия MAPI</span><span class="sxs-lookup"><span data-stu-id="fc89f-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="fc89f-123">Найдите строку MAPIXVER формы « _x.x.x_».</span><span class="sxs-lookup"><span data-stu-id="fc89f-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc89f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="fc89f-124">See also</span></span>



[<span data-ttu-id="fc89f-125">����� �������� � ���������������� MAPI</span><span class="sxs-lookup"><span data-stu-id="fc89f-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

