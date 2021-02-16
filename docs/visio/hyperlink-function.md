---
title: Функция HYPERLINK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Переходит на указанный адрес, который может быть путем к файлу, UNC или URL-адресу.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329948"
---
# <a name="hyperlink-function"></a><span data-ttu-id="0e105-103">Функция HYPERLINK</span><span class="sxs-lookup"><span data-stu-id="0e105-103">HYPERLINK Function</span></span>

<span data-ttu-id="0e105-104">Переходит на указанный адрес, который может быть путем к файлу, UNC или URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="0e105-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0e105-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e105-105">Syntax</span></span>

<span data-ttu-id="0e105-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span><span class="sxs-lookup"><span data-stu-id="0e105-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0e105-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e105-107">Parameters</span></span>

|<span data-ttu-id="0e105-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0e105-108">**Name**</span></span>|<span data-ttu-id="0e105-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0e105-109">**Required/Optional**</span></span>|<span data-ttu-id="0e105-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0e105-110">**Data Type**</span></span>|<span data-ttu-id="0e105-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e105-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0e105-112">_address_</span><span class="sxs-lookup"><span data-stu-id="0e105-112">_address_</span></span> <br/> |<span data-ttu-id="0e105-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0e105-113">Required</span></span>  <br/> |<span data-ttu-id="0e105-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0e105-114">**String**</span></span> <br/> |<span data-ttu-id="0e105-115">Полный или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="0e105-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="0e105-116">_subaddress_</span><span class="sxs-lookup"><span data-stu-id="0e105-116">_subaddress_</span></span> <br/> |<span data-ttu-id="0e105-117">Необязательна</span><span class="sxs-lookup"><span data-stu-id="0e105-117">Optional</span></span>  <br/> |<span data-ttu-id="0e105-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0e105-118">**String**</span></span> <br/> |<span data-ttu-id="0e105-119">Указывает расположение в адресе для ссылки.</span><span class="sxs-lookup"><span data-stu-id="0e105-119">Specifies a location within address to link to.</span></span> <span data-ttu-id="0e105-120">Например, если адрес — это файл Microsoft Visio, подадрес может быть именем страницы; если файл Microsoft Excel, подадрес может быть листа или диапазона в пределах листа; Если URL-адрес htmL-страницы, подадрес может быть привязкой.</span><span class="sxs-lookup"><span data-stu-id="0e105-120">For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="0e105-121">_extrainfo_</span><span class="sxs-lookup"><span data-stu-id="0e105-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="0e105-122">Необязательна</span><span class="sxs-lookup"><span data-stu-id="0e105-122">Optional</span></span>  <br/> |<span data-ttu-id="0e105-123">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0e105-123">**String**</span></span> <br/> |<span data-ttu-id="0e105-124">Передает сведения, используемые при разрешении URL-адреса, например координаты карты изображения.</span><span class="sxs-lookup"><span data-stu-id="0e105-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="0e105-125">_window_</span><span class="sxs-lookup"><span data-stu-id="0e105-125">_window_</span></span> <br/> |<span data-ttu-id="0e105-126">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0e105-126">Optional</span></span>  <br/> |<span data-ttu-id="0e105-127">**Логический**</span><span class="sxs-lookup"><span data-stu-id="0e105-127">**Boolean**</span></span> <br/> |<span data-ttu-id="0e105-128">Указывает, открывается ли гиперссылка в новом окне.</span><span class="sxs-lookup"><span data-stu-id="0e105-128">Specifies whether the hyperlink is opened in a new window.</span></span> <span data-ttu-id="0e105-129">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="0e105-129">The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="0e105-130">_frame_</span><span class="sxs-lookup"><span data-stu-id="0e105-130">_frame_</span></span> <br/> |<span data-ttu-id="0e105-131">Необязательна</span><span class="sxs-lookup"><span data-stu-id="0e105-131">Optional</span></span>  <br/> |<span data-ttu-id="0e105-132">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0e105-132">**String**</span></span> <br/> | <span data-ttu-id="0e105-133">Указывает имя кадра, на который необходимо нацелить, когда Visio открывается как активный документ в браузере ActiveX, например Microsoft Internet Explorer 3.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0e105-133">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later.</span></span> <span data-ttu-id="0e105-134">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="0e105-134">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e105-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e105-135">Remarks</span></span>

<span data-ttu-id="0e105-136">Если в документе нет базового пути, Visio переходит по этому пути.</span><span class="sxs-lookup"><span data-stu-id="0e105-136">If the document has no base path, Visio navigates according to the document path.</span></span> <span data-ttu-id="0e105-137">Если документ не был сохранен, гиперссылка не будет запределена.</span><span class="sxs-lookup"><span data-stu-id="0e105-137">If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="0e105-138">Относительные пути основаны  на базовом поле гиперссылки, указанном в диалоговом **окне "Свойства Visio".**</span><span class="sxs-lookup"><span data-stu-id="0e105-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="0e105-139">Вы можете использовать функцию GOTOPAGE для перемещения на страницы документа.</span><span class="sxs-lookup"><span data-stu-id="0e105-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0e105-140">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e105-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="0e105-141">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0e105-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="0e105-142">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0e105-142">Example 3</span></span>

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="0e105-143">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0e105-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

