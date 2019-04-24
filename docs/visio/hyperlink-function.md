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
description: Переходит по указанному адресу, который может быть URL-АДРЕСом файла, UNC-пути или URL-адреса.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329948"
---
# <a name="hyperlink-function"></a><span data-ttu-id="e51fb-103">Функция HYPERLINK</span><span class="sxs-lookup"><span data-stu-id="e51fb-103">HYPERLINK Function</span></span>

<span data-ttu-id="e51fb-104">Переходит по указанному адресу, который может быть URL-АДРЕСом файла, UNC-пути или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e51fb-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e51fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e51fb-105">Syntax</span></span>

<span data-ttu-id="e51fb-106">Гиперссылка ("\* \* *адрес* \* *" [, "* \*\* \* подадрес \* *", "* \* *extrainfo* \* \*", \* \* *окно* \* *, "* \* *Frame* \* \*"])</span><span class="sxs-lookup"><span data-stu-id="e51fb-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e51fb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e51fb-107">Parameters</span></span>

|<span data-ttu-id="e51fb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e51fb-108">**Name**</span></span>|<span data-ttu-id="e51fb-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e51fb-109">**Required/Optional**</span></span>|<span data-ttu-id="e51fb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e51fb-110">**Data Type**</span></span>|<span data-ttu-id="e51fb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e51fb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e51fb-112">_address_</span><span class="sxs-lookup"><span data-stu-id="e51fb-112">_address_</span></span> <br/> |<span data-ttu-id="e51fb-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e51fb-113">Required</span></span>  <br/> |<span data-ttu-id="e51fb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e51fb-114">**String**</span></span> <br/> |<span data-ttu-id="e51fb-115">Полный или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="e51fb-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="e51fb-116">_subaddress_</span><span class="sxs-lookup"><span data-stu-id="e51fb-116">_subaddress_</span></span> <br/> |<span data-ttu-id="e51fb-117">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="e51fb-117">Optional</span></span>  <br/> |<span data-ttu-id="e51fb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e51fb-118">**String**</span></span> <br/> |<span data-ttu-id="e51fb-119">Указывает расположение для ссылки в адресе.</span><span class="sxs-lookup"><span data-stu-id="e51fb-119">Specifies a location within address to link to.</span></span> <span data-ttu-id="e51fb-120">Например, если Address — это файл Microsoft Visio, подадрес может быть именем страницы; Если файл Microsoft Excel, подадрес может быть листом или диапазоном на листе; Если URL-адрес HTML-страницы, подадрес может быть привязкой.</span><span class="sxs-lookup"><span data-stu-id="e51fb-120">For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="e51fb-121">_ExtraInfo_</span><span class="sxs-lookup"><span data-stu-id="e51fb-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="e51fb-122">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="e51fb-122">Optional</span></span>  <br/> |<span data-ttu-id="e51fb-123">**String**</span><span class="sxs-lookup"><span data-stu-id="e51fb-123">**String**</span></span> <br/> |<span data-ttu-id="e51fb-124">Передает сведения, используемые при разрешении URL-адреса, такие как координаты карты ссылок.</span><span class="sxs-lookup"><span data-stu-id="e51fb-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="e51fb-125">_окно_</span><span class="sxs-lookup"><span data-stu-id="e51fb-125">_window_</span></span> <br/> |<span data-ttu-id="e51fb-126">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="e51fb-126">Optional</span></span>  <br/> |<span data-ttu-id="e51fb-127">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e51fb-127">**Boolean**</span></span> <br/> |<span data-ttu-id="e51fb-128">Указывает, следует ли открыть гиперссылку в новом окне.</span><span class="sxs-lookup"><span data-stu-id="e51fb-128">Specifies whether the hyperlink is opened in a new window.</span></span> <span data-ttu-id="e51fb-129">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="e51fb-129">The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="e51fb-130">_кадры_</span><span class="sxs-lookup"><span data-stu-id="e51fb-130">_frame_</span></span> <br/> |<span data-ttu-id="e51fb-131">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="e51fb-131">Optional</span></span>  <br/> |<span data-ttu-id="e51fb-132">**String**</span><span class="sxs-lookup"><span data-stu-id="e51fb-132">**String**</span></span> <br/> | <span data-ttu-id="e51fb-133">Задает имя конечного кадра при открытии Visio в качестве активного документа в браузере ActiveX, например Microsoft Internet Explorer 3,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e51fb-133">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later.</span></span> <span data-ttu-id="e51fb-134">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="e51fb-134">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e51fb-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e51fb-135">Remarks</span></span>

<span data-ttu-id="e51fb-136">Если у документа нет базового пути, Visio переходит в соответствии с путем к документу.</span><span class="sxs-lookup"><span data-stu-id="e51fb-136">If the document has no base path, Visio navigates according to the document path.</span></span> <span data-ttu-id="e51fb-137">Если документ не был сохранен, гиперссылка не определена.</span><span class="sxs-lookup"><span data-stu-id="e51fb-137">If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="e51fb-138">ОтНосительные пути зависят от поля **базы гиперссылки** , указанного в диалоговом окне " **свойства Visio** ".</span><span class="sxs-lookup"><span data-stu-id="e51fb-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="e51fb-139">С помощью функции GOTOPAGE можно переходить к страницам документа.</span><span class="sxs-lookup"><span data-stu-id="e51fb-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e51fb-140">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e51fb-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="e51fb-141">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e51fb-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="e51fb-142">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e51fb-142">Example 3</span></span>

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="e51fb-143">Пример 4</span><span class="sxs-lookup"><span data-stu-id="e51fb-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

