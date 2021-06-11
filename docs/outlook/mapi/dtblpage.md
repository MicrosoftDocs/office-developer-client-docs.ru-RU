---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424002"
---
# <a name="dtblpage"></a><span data-ttu-id="6cec6-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="6cec6-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="6cec6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cec6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cec6-105">Описывает страницу вкладок, которая будет использоваться в диалоговом окне, построенной из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="6cec6-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cec6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6cec6-106">Header file:</span></span>  <br/> |<span data-ttu-id="6cec6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cec6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6cec6-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="6cec6-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="6cec6-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="6cec6-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="6cec6-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="6cec6-110">Members</span></span>

 <span data-ttu-id="6cec6-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="6cec6-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="6cec6-112">Расположение в памяти метки строки символов для вкладки страницы.</span><span class="sxs-lookup"><span data-stu-id="6cec6-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="6cec6-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6cec6-113">**ulFlags**</span></span>
  
> <span data-ttu-id="6cec6-114">Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabelName.**</span><span class="sxs-lookup"><span data-stu-id="6cec6-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="6cec6-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6cec6-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="6cec6-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6cec6-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6cec6-117">Метка находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="6cec6-117">The label is in Unicode format.</span></span> <span data-ttu-id="6cec6-118">Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6cec6-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="6cec6-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="6cec6-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="6cec6-120">Расположение в памяти строки символов, определяющих **раздел [Сопоставления** файлов справки] в MAPISVC. Файл конфигурации INF или 0.</span><span class="sxs-lookup"><span data-stu-id="6cec6-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="6cec6-121">Имя файла, которое появляется в MAPISVC. Раздел INF может быть использован пользователем для доступа к расширенной справке для страницы вкладки, нажав кнопку **Справка** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6cec6-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="6cec6-122">Дополнительные сведения о записях в MAPISVC. INF см. [в файловом формате MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="6cec6-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="6cec6-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="6cec6-123">**ulContext**</span></span>
  
> <span data-ttu-id="6cec6-124">Уникальный идентификатор страницы вкладки в строке, определенной участником **ulbLpszComponent.**</span><span class="sxs-lookup"><span data-stu-id="6cec6-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="6cec6-125">Член **ulbLpszComponent** и **член ulContext** должны быть незеро для кнопки **справки** для работы.</span><span class="sxs-lookup"><span data-stu-id="6cec6-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="6cec6-126">Если этот идентификатор ноль, а строка компонентов NULL, то справки, связанной со страницей, не существует.</span><span class="sxs-lookup"><span data-stu-id="6cec6-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6cec6-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="6cec6-127">Remarks</span></span>

<span data-ttu-id="6cec6-128">Структура **DTBLPAGE** описывает страницу вкладок с управлением, которое используется для раздельного использования нескольких связанных диалоговых ящиков.</span><span class="sxs-lookup"><span data-stu-id="6cec6-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="6cec6-129">Обычно эти диалоговые окна являются листами свойств для отображения конфигурации, сообщений или параметров получателей.</span><span class="sxs-lookup"><span data-stu-id="6cec6-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="6cec6-130">Щелкнув вкладку, пользователь может переключиться с одного листа на другой.</span><span class="sxs-lookup"><span data-stu-id="6cec6-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="6cec6-131">Строка компонентов и идентификатор контекста предоставляют сведения о том, доступна ли расширенная справка для страницы вкладки.</span><span class="sxs-lookup"><span data-stu-id="6cec6-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="6cec6-132">Если расширенная справка доступна, строка компонентов и идентификатор контекста предоставляют сведения о доступе к ней.</span><span class="sxs-lookup"><span data-stu-id="6cec6-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="6cec6-133">Строка компонентов карты в файл справки; идентификатор контекста карты начальной темы справки.</span><span class="sxs-lookup"><span data-stu-id="6cec6-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="6cec6-134">Если идентификатор контекста нулевой, а строка компонентов NULL, расширенная справка недоступна.</span><span class="sxs-lookup"><span data-stu-id="6cec6-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="6cec6-135">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6cec6-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="6cec6-136">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="6cec6-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6cec6-137">См. также</span><span class="sxs-lookup"><span data-stu-id="6cec6-137">See also</span></span>



[<span data-ttu-id="6cec6-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="6cec6-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="6cec6-139">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="6cec6-139">MAPI Structures</span></span>](mapi-structures.md)

