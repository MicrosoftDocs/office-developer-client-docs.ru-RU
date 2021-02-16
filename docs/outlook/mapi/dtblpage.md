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
# <a name="dtblpage"></a><span data-ttu-id="5a1c6-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="5a1c6-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="5a1c6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a1c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a1c6-105">Описывает страницу вкладок, которая будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a1c6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5a1c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a1c6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a1c6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5a1c6-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="5a1c6-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="5a1c6-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="5a1c6-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="5a1c6-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="5a1c6-110">Members</span></span>

 <span data-ttu-id="5a1c6-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="5a1c6-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="5a1c6-112">Положение в памяти подписи строки символа для вкладки страницы.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="5a1c6-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5a1c6-113">**ulFlags**</span></span>
  
> <span data-ttu-id="5a1c6-114">Битовая метка флагов, используемая для обозначения формата метки, на который указывает член **ulbLpszLabelName.**</span><span class="sxs-lookup"><span data-stu-id="5a1c6-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="5a1c6-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5a1c6-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="5a1c6-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5a1c6-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5a1c6-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-117">The label is in Unicode format.</span></span> <span data-ttu-id="5a1c6-118">Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="5a1c6-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="5a1c6-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="5a1c6-120">Положение в памяти строки символа, определяющий **раздел [Сопоставления** файлов справки] в MAPISVC. INF-файл конфигурации или 0.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="5a1c6-121">Имя файла, которое появляется в MAPISVC. Пользователь может использовать раздел INF для доступа к расширенной справке  для страницы вкладок, нажав кнопку "Справка" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="5a1c6-122">Дополнительные сведения о записях в MAPISVC. INF, [см. формат файла MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="5a1c6-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="5a1c6-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="5a1c6-123">**ulContext**</span></span>
  
> <span data-ttu-id="5a1c6-124">Уникальный идентификатор страницы вкладок в строке, определенной членом **ulbLpszComponent.**</span><span class="sxs-lookup"><span data-stu-id="5a1c6-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="5a1c6-125">Для работы кнопки "Справка" оба члена **ulbLpszComponent** и  **ulContext** должны быть ненулями.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="5a1c6-126">Если этот идентификатор имеет нулевое значение, а строка компонента имеет значение NULL, справка, связанная со страницей, не существует.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5a1c6-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a1c6-127">Remarks</span></span>

<span data-ttu-id="5a1c6-128">Структура **DTBLPAGE** описывает страницу вкладок, которая используется для разбиения нескольких связанных диалоговых окной.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="5a1c6-129">Как правило, эти диалоговые окна являются листами свойств для отображения параметров конфигурации, сообщений или получателей.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="5a1c6-130">Щелкнув вкладку, пользователь может переключиться с одного листа на другой.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="5a1c6-131">Строка компонента и идентификатор контекста предоставляют сведения о том, доступна ли расширенная справка для страницы вкладок.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="5a1c6-132">Если доступна расширенная справка, строка компонента и идентификатор контекста будут предоставлять сведения о том, как получить к ней доступ.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="5a1c6-133">Строка компонента сопо карте с файлом справки; идентификатор контекста сопозначит с начальным разделом справки.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="5a1c6-134">Если идентификатор контекста — ноль, а строка компонента NULL, расширенная справка недоступна.</span><span class="sxs-lookup"><span data-stu-id="5a1c6-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="5a1c6-135">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="5a1c6-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="5a1c6-136">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="5a1c6-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a1c6-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5a1c6-137">See also</span></span>



[<span data-ttu-id="5a1c6-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="5a1c6-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="5a1c6-139">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5a1c6-139">MAPI Structures</span></span>](mapi-structures.md)

