---
title: Сведения об API аварийного восстановления MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576591"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="bb483-103">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="bb483-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="bb483-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb483-105">API сбой восстановления MAPI, проверяет состояние файл личных папок (PST) или файл автономной папки (OST) общей памяти для проверки правильности данных в стабильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="bb483-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="bb483-106">Если он установлен в стабильном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные из open PST и OST на диске и блокирует PST и OST и не позволяет любой доступ на чтение или запись доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="bb483-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="bb483-107">Это гарантирует, что данные остается в стабильном состоянии, пока процесс завершается.</span><span class="sxs-lookup"><span data-stu-id="bb483-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="bb483-108">Убедитесь, что PST и OST в стабильном состоянии до завершения процесса, позволяет предотвратить отображение следующее сообщение об ошибке Microsoft Outlook 2013 и Microsoft Outlook 2010 и избежать проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="bb483-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="bb483-109">**Файл данных не закрыта должным образом время последнего он использовался и выполняется проверка проблем. Может повлиять на производительность во время выполнения проверки.**</span><span class="sxs-lookup"><span data-stu-id="bb483-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="bb483-110">Этот интерфейс API предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="bb483-110">This API provides the following:</span></span>
  
<span data-ttu-id="bb483-111">Константы:</span><span class="sxs-lookup"><span data-stu-id="bb483-111">Constants:</span></span>
  
- [<span data-ttu-id="bb483-112">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="bb483-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="bb483-113">Функции:</span><span class="sxs-lookup"><span data-stu-id="bb483-113">Functions:</span></span>
  
- [<span data-ttu-id="bb483-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="bb483-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="bb483-115">См. также</span><span class="sxs-lookup"><span data-stu-id="bb483-115">See also</span></span>



[<span data-ttu-id="bb483-116">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="bb483-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

