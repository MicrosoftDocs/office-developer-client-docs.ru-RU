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
# <a name="fixmapi"></a><span data-ttu-id="dab15-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="dab15-103">FixMAPI</span></span>

  
  
<span data-ttu-id="dab15-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dab15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dab15-105">Создает резервную копию текущей копии mapi32.dll на клиентском компьютере и восстанавливает mapi32.dll с помощью библиотеки загона MAPI, mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="dab15-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dab15-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="dab15-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dab15-107">Экспортируется с помощью:</span><span class="sxs-lookup"><span data-stu-id="dab15-107">Exported by:</span></span>  <br/> |<span data-ttu-id="dab15-108">mapistub.dll</span><span class="sxs-lookup"><span data-stu-id="dab15-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="dab15-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="dab15-109">Called by:</span></span>  <br/> |<span data-ttu-id="dab15-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="dab15-110">Client</span></span>  <br/> |
|<span data-ttu-id="dab15-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="dab15-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="dab15-112">Windows</span><span class="sxs-lookup"><span data-stu-id="dab15-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="dab15-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dab15-113">Return values</span></span>

<span data-ttu-id="dab15-114">В случае успешного функционирования функции возвращаемая величина не является нулем.</span><span class="sxs-lookup"><span data-stu-id="dab15-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="dab15-115">Если функция не работает, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="dab15-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="dab15-116">Чтобы получить расширенные сведения об ошибках, вызовите функцию Microsoft Windows Software Development Kit (SDK) **[GetLastError.](https://msdn.microsoft.com/library/ms679360.aspx)**</span><span class="sxs-lookup"><span data-stu-id="dab15-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dab15-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="dab15-117">Remarks</span></span>

 <span data-ttu-id="dab15-118">**FixMAPI** не заменяет текущий файл mapi32.dll, если он помечен как "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="dab15-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="dab15-119">**FixMAPI** не заменяет текущий mapi32.dll если Microsoft Exchange Server установлен на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dab15-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="dab15-120">Когда **FixMAPI** создает резервную копию текущей копии mapi32.dll на компьютере, он присваивает резервной копии имя, которое отличается от "mapi32.dll".</span><span class="sxs-lookup"><span data-stu-id="dab15-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="dab15-121">Затем он направляет последующие вызовы, предназначенные для этой сборки, в резервную копию.</span><span class="sxs-lookup"><span data-stu-id="dab15-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dab15-122">См. также</span><span class="sxs-lookup"><span data-stu-id="dab15-122">See also</span></span>



[<span data-ttu-id="dab15-123">KB 256946: при запуске Outlook 2000 вы получаете сообщение о конфликте программы</span><span class="sxs-lookup"><span data-stu-id="dab15-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="dab15-124">KB 228457: описание средства Fixmapi.exe, включенного в Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="dab15-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

