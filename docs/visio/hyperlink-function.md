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
description: Переходит по указанному адресу, который может быть файл, UNC или URL-адрес путь.
ms.openlocfilehash: 4e86fd3682d5d9e26c52839e76d2016d654b3141
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19813917"
---
# <a name="hyperlink-function"></a><span data-ttu-id="96414-103">Функция HYPERLINK</span><span class="sxs-lookup"><span data-stu-id="96414-103">HYPERLINK Function</span></span>

<span data-ttu-id="96414-104">Переходит по указанному адресу, который может быть файл, UNC или URL-адрес путь.</span><span class="sxs-lookup"><span data-stu-id="96414-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="96414-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96414-105">Syntax</span></span>

<span data-ttu-id="96414-106">Гиперссылка ("** *адрес* **" [,"** *дополнительный адрес* **","** *extrainfo* **", ** *окно* **, "** *frame* **"])</span><span class="sxs-lookup"><span data-stu-id="96414-106">HYPERLINK(" ** *address* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="96414-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="96414-107">Parameters</span></span>

|<span data-ttu-id="96414-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="96414-108">**Name**</span></span>|<span data-ttu-id="96414-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="96414-109">**Required/Optional**</span></span>|<span data-ttu-id="96414-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="96414-110">**Data Type**</span></span>|<span data-ttu-id="96414-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96414-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="96414-112">_адрес_</span><span class="sxs-lookup"><span data-stu-id="96414-112">_address_</span></span> <br/> |<span data-ttu-id="96414-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96414-113">Required</span></span>  <br/> |<span data-ttu-id="96414-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="96414-114">**String**</span></span> <br/> |<span data-ttu-id="96414-115">Полный путь или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="96414-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="96414-116">_Дополнительный адрес_</span><span class="sxs-lookup"><span data-stu-id="96414-116">_subaddress_</span></span> <br/> |<span data-ttu-id="96414-117">Optional</span><span class="sxs-lookup"><span data-stu-id="96414-117">Optional</span></span>  <br/> |<span data-ttu-id="96414-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="96414-118">**String**</span></span> <br/> |<span data-ttu-id="96414-119">Указывает расположение в адрес, который необходимо связать с.</span><span class="sxs-lookup"><span data-stu-id="96414-119">Specifies a location within address to link to.</span></span> <span data-ttu-id="96414-120">Например если адрес файл Microsoft Visio, дополнительный адрес может быть имя страницы; Если файл Microsoft Excel, дополнительный адрес может быть электронной таблицы или диапазон в электронной таблице; Если URL-адрес страницы HTML, дополнительный адрес может быть привязки.</span><span class="sxs-lookup"><span data-stu-id="96414-120">For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="96414-121">_ExtraInfo_</span><span class="sxs-lookup"><span data-stu-id="96414-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="96414-122">Optional</span><span class="sxs-lookup"><span data-stu-id="96414-122">Optional</span></span>  <br/> |<span data-ttu-id="96414-123">**Строка**</span><span class="sxs-lookup"><span data-stu-id="96414-123">**String**</span></span> <br/> |<span data-ttu-id="96414-124">Передает данные, используемые в разрешении URL-адрес, например координаты гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="96414-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="96414-125">_окно_</span><span class="sxs-lookup"><span data-stu-id="96414-125">_window_</span></span> <br/> |<span data-ttu-id="96414-126">Optional</span><span class="sxs-lookup"><span data-stu-id="96414-126">Optional</span></span>  <br/> |<span data-ttu-id="96414-127">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="96414-127">**Boolean**</span></span> <br/> |<span data-ttu-id="96414-128">Указывает, будет ли гиперссылка открывается в новом окне.</span><span class="sxs-lookup"><span data-stu-id="96414-128">Specifies whether the hyperlink is opened in a new window.</span></span> <span data-ttu-id="96414-129">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="96414-129">The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="96414-130">_кадров_</span><span class="sxs-lookup"><span data-stu-id="96414-130">_frame_</span></span> <br/> |<span data-ttu-id="96414-131">Optional</span><span class="sxs-lookup"><span data-stu-id="96414-131">Optional</span></span>  <br/> |<span data-ttu-id="96414-132">**Строка**</span><span class="sxs-lookup"><span data-stu-id="96414-132">**String**</span></span> <br/> | <span data-ttu-id="96414-133">Указывает имя рамки для конечного при открытом как активный документ в браузере ActiveX, такие как Microsoft Internet Explorer 3.0 или более поздней версии Visio.</span><span class="sxs-lookup"><span data-stu-id="96414-133">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later.</span></span> <span data-ttu-id="96414-134">По умолчанию используется пустая строка.</span><span class="sxs-lookup"><span data-stu-id="96414-134">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96414-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="96414-135">Remarks</span></span>

<span data-ttu-id="96414-136">Если в документе есть путь не базового, Visio переходит в соответствии с путь к документу.</span><span class="sxs-lookup"><span data-stu-id="96414-136">If the document has no base path, Visio navigates according to the document path.</span></span> <span data-ttu-id="96414-137">Если документ не был сохранен, гиперссылки не определено.</span><span class="sxs-lookup"><span data-stu-id="96414-137">If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="96414-138">Относительные пути основаны на поле **базового гиперссылки** , указанных в диалоговом окне **Свойства Visio** .</span><span class="sxs-lookup"><span data-stu-id="96414-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="96414-139">Функция НАСТРАНИЦУ перейдите к страницам документа.</span><span class="sxs-lookup"><span data-stu-id="96414-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="96414-140">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96414-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="96414-141">Пример 2</span><span class="sxs-lookup"><span data-stu-id="96414-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="96414-142">Пример 3</span><span class="sxs-lookup"><span data-stu-id="96414-142">Example 3</span></span>

 `HYPERLINK("http://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="96414-143">Пример 4</span><span class="sxs-lookup"><span data-stu-id="96414-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

