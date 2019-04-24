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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340119"
---
# <a name="dtblpage"></a><span data-ttu-id="19d83-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="19d83-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="19d83-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19d83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19d83-105">Описывает страницу с вкладками, которая будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="19d83-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19d83-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="19d83-106">Header file:</span></span>  <br/> |<span data-ttu-id="19d83-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="19d83-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="19d83-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="19d83-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="19d83-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="19d83-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="19d83-110">Members</span><span class="sxs-lookup"><span data-stu-id="19d83-110">Members</span></span>

 <span data-ttu-id="19d83-111">**Улблпсзлабел**</span><span class="sxs-lookup"><span data-stu-id="19d83-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="19d83-112">Позиция в памяти подписи строки символов для вкладки страницы.</span><span class="sxs-lookup"><span data-stu-id="19d83-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="19d83-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="19d83-113">**ulFlags**</span></span>
  
> <span data-ttu-id="19d83-114">Битовая маска флагов, используемых для обозначения формата метки, на который указывает элемент **улблпсзлабелнаме** .</span><span class="sxs-lookup"><span data-stu-id="19d83-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="19d83-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="19d83-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="19d83-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="19d83-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="19d83-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="19d83-117">The label is in Unicode format.</span></span> <span data-ttu-id="19d83-118">Если флаг МАПИ_УНИКОДЕ не установлен, метка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="19d83-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="19d83-119">**Улблпсзкомпонент**</span><span class="sxs-lookup"><span data-stu-id="19d83-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="19d83-120">Позиция в памяти строки символов, указывающей раздел **[Help File Mappings]** в Mapisvc. INF-файл конфигурации или 0.</span><span class="sxs-lookup"><span data-stu-id="19d83-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="19d83-121">Имя файла, отображаемое в MAPISVC. Раздел INF может использоваться пользователем для доступа к расширенной справке для страницы с вкладками, нажав кнопку **Справка** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="19d83-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="19d83-122">Дополнительные сведения о записях в MAPISVC. INF в разделе [Формат файлов Mapisvc. INF-файл](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="19d83-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="19d83-123">**Улконтекст**</span><span class="sxs-lookup"><span data-stu-id="19d83-123">**ulContext**</span></span>
  
> <span data-ttu-id="19d83-124">Уникальный идентификатор для страницы с вкладками в строке, определенной элементом **улблпсзкомпонент** .</span><span class="sxs-lookup"><span data-stu-id="19d83-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="19d83-125">Элемент **улблпсзкомпонент** и элемент **улконтекст** должны быть ненулевыми, чтобы кнопка **справки** работала.</span><span class="sxs-lookup"><span data-stu-id="19d83-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="19d83-126">Если этот идентификатор равен нулю, а строка компонента имеет значение NULL, Справка, связанная со страницей, отсутствует.</span><span class="sxs-lookup"><span data-stu-id="19d83-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="19d83-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19d83-127">Remarks</span></span>

<span data-ttu-id="19d83-128">Структура **дтблпаже** описывает элемент управления с вкладками, который используется для разделения нескольких связанных диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="19d83-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="19d83-129">Как правило, эти диалоговые окна являются страницами свойств для отображения параметров конфигурации, сообщений или получателей.</span><span class="sxs-lookup"><span data-stu-id="19d83-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="19d83-130">Если щелкнуть вкладку, пользователь может переключаться с одного листа на другой.</span><span class="sxs-lookup"><span data-stu-id="19d83-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="19d83-131">Строка компонента и идентификатор контекста содержат сведения о том, доступна ли расширенная Справка для вкладки.</span><span class="sxs-lookup"><span data-stu-id="19d83-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="19d83-132">Если доступна расширенная Справка, строка компонента и идентификатор контекста будут содержать сведения о том, как получить к нему доступ.</span><span class="sxs-lookup"><span data-stu-id="19d83-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="19d83-133">Строка компонента сопоставляется с файлом справки; Идентификатор контекста сопоставляется с исходным разделом справки.</span><span class="sxs-lookup"><span data-stu-id="19d83-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="19d83-134">Если идентификатор контекста равен нулю, а строка компонента имеет значение NULL, расширенная Справка недоступна.</span><span class="sxs-lookup"><span data-stu-id="19d83-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="19d83-135">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="19d83-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="19d83-136">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="19d83-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19d83-137">См. также</span><span class="sxs-lookup"><span data-stu-id="19d83-137">See also</span></span>



[<span data-ttu-id="19d83-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="19d83-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="19d83-139">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="19d83-139">MAPI Structures</span></span>](mapi-structures.md)

