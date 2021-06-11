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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334963"
---
# <a name="fixmapi"></a><span data-ttu-id="eff5e-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="eff5e-103">FixMAPI</span></span>

  
  
<span data-ttu-id="eff5e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eff5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eff5e-105">Создает копию резервного копирования текущей копии mapi32.dll на клиентском компьютере и восстанавливает mapi32.dll с помощью библиотеки mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="eff5e-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="eff5e-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="eff5e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eff5e-107">Экспортируемая по:</span><span class="sxs-lookup"><span data-stu-id="eff5e-107">Exported by:</span></span>  <br/> |<span data-ttu-id="eff5e-108">mapistub.dll</span><span class="sxs-lookup"><span data-stu-id="eff5e-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="eff5e-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="eff5e-109">Called by:</span></span>  <br/> |<span data-ttu-id="eff5e-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="eff5e-110">Client</span></span>  <br/> |
|<span data-ttu-id="eff5e-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="eff5e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="eff5e-112">Windows</span><span class="sxs-lookup"><span data-stu-id="eff5e-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="eff5e-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="eff5e-113">Return values</span></span>

<span data-ttu-id="eff5e-114">Если функция будет успешной, возвращаемая сумма не будет нулевой.</span><span class="sxs-lookup"><span data-stu-id="eff5e-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="eff5e-115">Если функция не работает, возвращается значение ноль.</span><span class="sxs-lookup"><span data-stu-id="eff5e-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="eff5e-116">Чтобы получить расширенные сведения об ошибках, позвоните в функцию Microsoft Windows Software Development Kit (SDK) **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="eff5e-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eff5e-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="eff5e-117">Remarks</span></span>

 <span data-ttu-id="eff5e-118">**FixMAPI** не заменяет текущий файл mapi32.dll, если файл помечен как только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eff5e-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="eff5e-119">**FixMAPI** не заменяет текущий mapi32.dll, Microsoft Exchange Server установлен на компьютере.</span><span class="sxs-lookup"><span data-stu-id="eff5e-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="eff5e-120">Когда **FixMAPI** создает копию резервного копирования текущей копии mapi32.dll на компьютере, она назначает копию резервной копии имя, отличаее от "mapi32.dll".</span><span class="sxs-lookup"><span data-stu-id="eff5e-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="eff5e-121">Затем он направляет последующие вызовы, предназначенные для этой сборки, в копию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="eff5e-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eff5e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="eff5e-122">See also</span></span>



[<span data-ttu-id="eff5e-123">KB 256946. При запуске Outlook 2000 г. вы получаете сообщение об ошибке конфликта программы</span><span class="sxs-lookup"><span data-stu-id="eff5e-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="eff5e-124">KB 228457: Описание средства Fixmapi.exe, включенного в Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="eff5e-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

