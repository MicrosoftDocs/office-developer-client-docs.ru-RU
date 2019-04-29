---
title: Функция OPENFILE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Открывает документ Microsoft Visio, если он еще не открыт, и активирует окно документа.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419578"
---
# <a name="openfile-function"></a><span data-ttu-id="35654-103">Функция OPENFILE</span><span class="sxs-lookup"><span data-stu-id="35654-103">OPENFILE Function</span></span>

<span data-ttu-id="35654-104">Открывает документ Microsoft Visio, если он еще не открыт, и активирует окно документа.</span><span class="sxs-lookup"><span data-stu-id="35654-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="35654-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35654-105">Syntax</span></span>

 <span data-ttu-id="35654-106">**OPENFILE** ( _"filename"_)</span><span class="sxs-lookup"><span data-stu-id="35654-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="35654-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="35654-107">Parameters</span></span>

|<span data-ttu-id="35654-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="35654-108">**Name**</span></span>|<span data-ttu-id="35654-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="35654-109">**Required/Optional**</span></span>|<span data-ttu-id="35654-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="35654-110">**Data Type**</span></span>|<span data-ttu-id="35654-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35654-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35654-112">_задан_</span><span class="sxs-lookup"><span data-stu-id="35654-112">_filename_</span></span> <br/> |<span data-ttu-id="35654-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35654-113">Required</span></span>  <br/> |<span data-ttu-id="35654-114">**String**</span><span class="sxs-lookup"><span data-stu-id="35654-114">**String**</span></span> <br/> |<span data-ttu-id="35654-115">Имя файла, включая путь к файлу, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="35654-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35654-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="35654-116">Remarks</span></span>

<span data-ttu-id="35654-117">Несколько вызовов функций OPENFILE ставятся в очередь и выполняются в порядке оценки.</span><span class="sxs-lookup"><span data-stu-id="35654-117">Multiple OPENFILE function calls are queued and executed in order of evaluation.</span></span> <span data-ttu-id="35654-118">Если текущий документ Visio активирован для редактирования на визуальном (на месте), запускается новый экземпляр Visio с запрошенным именем файла.</span><span class="sxs-lookup"><span data-stu-id="35654-118">If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="35654-119">Эта функция всегда возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="35654-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="35654-120">В более ранних версиях приложения Visio Эта функция отображается как _ОПЕНФИЛЕ.</span><span class="sxs-lookup"><span data-stu-id="35654-120">In earlier versions of the Visio application, this function appears as _OPENFILE.</span></span> <span data-ttu-id="35654-121">Visio версии 4,0 и более поздних принимают любой из этих стилей.</span><span class="sxs-lookup"><span data-stu-id="35654-121">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="35654-122">Пример</span><span class="sxs-lookup"><span data-stu-id="35654-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="35654-123">Открывает указанный файл "MyFile. vsdx" в новом окне или активирует окно, если файл уже открыт.</span><span class="sxs-lookup"><span data-stu-id="35654-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

