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
ms.openlocfilehash: bd0caff8a6c7834bdd01ef4be64805bde66dd6d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578824"
---
# <a name="dtblpage"></a><span data-ttu-id="3cd5c-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="3cd5c-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="3cd5c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cd5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cd5c-105">Описание, который будет использоваться в диалоговом окне, построенного из таблицы отображения страницы с вкладками.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3cd5c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3cd5c-106">Header file:</span></span>  <br/> |<span data-ttu-id="3cd5c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cd5c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3cd5c-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="3cd5c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="3cd5c-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="3cd5c-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="3cd5c-110">Members</span><span class="sxs-lookup"><span data-stu-id="3cd5c-110">Members</span></span>

 <span data-ttu-id="3cd5c-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="3cd5c-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="3cd5c-112">Положение в памяти метки строка символов для вкладку страница.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="3cd5c-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3cd5c-113">**ulFlags**</span></span>
  
> <span data-ttu-id="3cd5c-114">Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="3cd5c-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="3cd5c-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3cd5c-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="3cd5c-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3cd5c-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3cd5c-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-117">The label is in Unicode format.</span></span> <span data-ttu-id="3cd5c-118">Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="3cd5c-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="3cd5c-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="3cd5c-120">Положение в памяти строку символов, идентифицирующий в разделе **[Help File Mappings]** в файл Mapisvc.inf. INF-файл конфигурации, либо 0.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="3cd5c-121">Имя файла, отображаемое в файл Mapisvc.inf. Можно использовать раздел INF пользователем, для доступа к расширенному справки для вкладки, нажав кнопку **Справка** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="3cd5c-122">Дополнительные сведения о записи в файл Mapisvc.inf. INF, видеть [файл формата из файл Mapisvc.inf. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="3cd5c-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="3cd5c-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="3cd5c-123">**ulContext**</span></span>
  
> <span data-ttu-id="3cd5c-124">Уникальный идентификатор для вкладки в строке, определенные в элемент **ulbLpszComponent** .</span><span class="sxs-lookup"><span data-stu-id="3cd5c-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="3cd5c-125">Член **ulbLpszComponent** и член **ulContext** должны быть ненулевое кнопки **Справка** для работы.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="3cd5c-126">Если этот идентификатор равно нулю, и компонент строки имеет значение NULL, нет нет справки, связанные со страницей.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3cd5c-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="3cd5c-127">Remarks</span></span>

<span data-ttu-id="3cd5c-128">Структура **DTBLPAGE** описывает страницы с вкладками элемент управления, который используется для разделения нескольких связанных диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="3cd5c-129">Как правило эти диалоговые окна, страницы свойств для отображения конфигурации, сообщение или получателей параметры.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="3cd5c-130">Щелкнув вкладку, можно переключаться из одного листа в другую.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="3cd5c-131">Идентификатор компонента строки и контекста содержатся сведения о расширенных Справка доступна для страницы с вкладками.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="3cd5c-132">При наличии расширенной справки строки и контекста идентификатор компонента предоставляются сведения о том, как получить к нему доступ.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="3cd5c-133">Компонент строки соответствует этот файл; Идентификатор контекста сопоставляет начальной раздел справки.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="3cd5c-134">Если идентификатор контекста равно нулю, а строка компонент имеет значение NULL, расширенные Справка недоступна.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="3cd5c-135">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3cd5c-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3cd5c-136">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="3cd5c-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3cd5c-137">См. также</span><span class="sxs-lookup"><span data-stu-id="3cd5c-137">See also</span></span>



[<span data-ttu-id="3cd5c-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3cd5c-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="3cd5c-139">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3cd5c-139">MAPI Structures</span></span>](mapi-structures.md)

