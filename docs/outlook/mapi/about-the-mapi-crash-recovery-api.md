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
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="0d03a-103">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="0d03a-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="0d03a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d03a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d03a-105">API восстановления после сбоя MAPI проверяет состояние общей памяти PST-файла личных папок (PST) или файла автономных папок (OST), чтобы убедиться, что данные находятся в согласованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="0d03a-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="0d03a-106">Если он находится в согласованном состоянии, функция [мапикрашрековери](mapicrashrecovery.md) перемещает данные из открытых PST-файлов или остс на диск и блокирует PST-файлы или остс и не разрешает доступ к данным для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="0d03a-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="0d03a-107">Это гарантирует, что данные остаются в согласованном состоянии до завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="0d03a-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="0d03a-108">Убедившись, что PST-файлы или Остс находятся в согласованном состоянии до завершения процесса, можно запретить Microsoft Outlook 2013 и Microsoft Outlook 2010 отображать следующее сообщение об ошибке и избежать проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="0d03a-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="0d03a-109">**Файл данных не был правильно закрыт при последнем использовании и проверяется на наличие проблем. В процессе проверки производительность может быть снижена.**</span><span class="sxs-lookup"><span data-stu-id="0d03a-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="0d03a-110">Этот API предоставляет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="0d03a-110">This API provides the following:</span></span>
  
<span data-ttu-id="0d03a-111">Применяем</span><span class="sxs-lookup"><span data-stu-id="0d03a-111">Constants:</span></span>
  
- [<span data-ttu-id="0d03a-112">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="0d03a-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="0d03a-113">Обязанностей</span><span class="sxs-lookup"><span data-stu-id="0d03a-113">Functions:</span></span>
  
- [<span data-ttu-id="0d03a-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="0d03a-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="0d03a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0d03a-115">See also</span></span>



[<span data-ttu-id="0d03a-116">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="0d03a-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

