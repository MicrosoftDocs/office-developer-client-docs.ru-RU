---
title: Сведения об API аварийного восстановления MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420264"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="53611-103">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="53611-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="53611-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53611-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53611-105">API аварийного восстановления MAPI проверяет состояние файла персональных папок (PST) или файла автономных папок (OST), чтобы убедиться, что данные в согласованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="53611-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="53611-106">Если оно находится в согласованном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные из открытых PSTs или OSTs на диск и блокирует PSTs или OSTs и не позволяет читать или записывать доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="53611-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="53611-107">Это гарантирует, что данные остаются в согласованном состоянии до окончания процесса.</span><span class="sxs-lookup"><span data-stu-id="53611-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="53611-108">Гарантируя, что psTs или OSTs находятся в согласованном состоянии до прекращения процесса, вы можете запретить Microsoft Outlook 2013 и Microsoft Outlook 2010, русская версия отобразить следующее сообщение об ошибке и избежать проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="53611-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="53611-109">**Файл данных не закрывался должным образом при последнем использовании и проверяется на наличие проблем. Производительность может быть затронута во время проверки.**</span><span class="sxs-lookup"><span data-stu-id="53611-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="53611-110">В этом API содержится следующее:</span><span class="sxs-lookup"><span data-stu-id="53611-110">This API provides the following:</span></span>
  
<span data-ttu-id="53611-111">Константы:</span><span class="sxs-lookup"><span data-stu-id="53611-111">Constants:</span></span>
  
- [<span data-ttu-id="53611-112">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="53611-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="53611-113">Функции:</span><span class="sxs-lookup"><span data-stu-id="53611-113">Functions:</span></span>
  
- [<span data-ttu-id="53611-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="53611-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="53611-115">См. также</span><span class="sxs-lookup"><span data-stu-id="53611-115">See also</span></span>



[<span data-ttu-id="53611-116">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="53611-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

