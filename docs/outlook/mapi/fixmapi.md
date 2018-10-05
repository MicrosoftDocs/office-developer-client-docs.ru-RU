---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383816"
---
# <a name="fixmapi"></a><span data-ttu-id="818fa-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="818fa-103">FixMAPI</span></span>

  
  
<span data-ttu-id="818fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="818fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="818fa-105">Делает резервную копию текущего копию mapi32.dll на стороне клиента, компьютер и восстанавливает mapi32.dll с библиотекой заглушка MAPI, mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="818fa-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="818fa-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="818fa-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818fa-107">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="818fa-107">Exported by:</span></span>  <br/> |<span data-ttu-id="818fa-108">MAPISTUB.dll</span><span class="sxs-lookup"><span data-stu-id="818fa-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="818fa-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="818fa-109">Called by:</span></span>  <br/> |<span data-ttu-id="818fa-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="818fa-110">Client</span></span>  <br/> |
|<span data-ttu-id="818fa-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="818fa-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="818fa-112">"Windows";</span><span class="sxs-lookup"><span data-stu-id="818fa-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="818fa-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="818fa-113">Return values</span></span>

<span data-ttu-id="818fa-114">Если функция успешно выполнена, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="818fa-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="818fa-115">Если функция завершается с ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="818fa-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="818fa-116">Чтобы получить расширенные сведения об ошибке, вызовите функцию комплект разработки программного обеспечения (SDK) Windows Microsoft, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="818fa-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="818fa-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="818fa-117">Remarks</span></span>

 <span data-ttu-id="818fa-118">**FixMAPI** не заменяет текущий файл mapi32.dll, если файл помечен как доступный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="818fa-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="818fa-119">**FixMAPI** не заменяет текущий mapi32.dll, если на компьютере установлен Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="818fa-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="818fa-120">Когда **FixMAPI** создает резервную копию текущего копию mapi32.dll на компьютере, назначает резервной копии имя, отличное от «mapi32.dll».</span><span class="sxs-lookup"><span data-stu-id="818fa-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="818fa-121">Затем переходит последующих вызовов, предназначенный для этой сборке для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="818fa-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="818fa-122">См. также</span><span class="sxs-lookup"><span data-stu-id="818fa-122">See also</span></span>



[<span data-ttu-id="818fa-123">Статья БАЗЫ знаний 256946:, Вы получаете сообщение об ошибке конфликта программы при запуске Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="818fa-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="818fa-124">Статья БАЗЫ знаний 228457: Описание средства Fixmapi.exe входит в состав Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="818fa-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

