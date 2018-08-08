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
description: Открывает документ Microsoft Visio, если он еще не открыт и активирует окно документа.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814319"
---
# <a name="openfile-function"></a><span data-ttu-id="df854-103">Функция OPENFILE</span><span class="sxs-lookup"><span data-stu-id="df854-103">OPENFILE Function</span></span>

<span data-ttu-id="df854-104">Открывает документ Microsoft Visio, если он еще не открыт и активирует окно документа.</span><span class="sxs-lookup"><span data-stu-id="df854-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="df854-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df854-105">Syntax</span></span>

 <span data-ttu-id="df854-106">**OPENFILE** ( _«имя файла»_)</span><span class="sxs-lookup"><span data-stu-id="df854-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="df854-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="df854-107">Parameters</span></span>

|<span data-ttu-id="df854-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="df854-108">**Name**</span></span>|<span data-ttu-id="df854-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="df854-109">**Required/Optional**</span></span>|<span data-ttu-id="df854-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="df854-110">**Data Type**</span></span>|<span data-ttu-id="df854-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df854-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df854-112">_Имя файла_</span><span class="sxs-lookup"><span data-stu-id="df854-112">_filename_</span></span> <br/> |<span data-ttu-id="df854-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df854-113">Required</span></span>  <br/> |<span data-ttu-id="df854-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="df854-114">**String**</span></span> <br/> |<span data-ttu-id="df854-115">Имя файла, включая путь к файлу, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="df854-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df854-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="df854-116">Remarks</span></span>

<span data-ttu-id="df854-117">Несколько вызовов функций OPENFILE в очередь и выполняются в порядок вычисления.</span><span class="sxs-lookup"><span data-stu-id="df854-117">Multiple OPENFILE function calls are queued and executed in order of evaluation.</span></span> <span data-ttu-id="df854-118">Если текущий документ Visio активирован для визуального редактирования (на месте), новый экземпляр Visio запускается с именем запрошенный файл.</span><span class="sxs-lookup"><span data-stu-id="df854-118">If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="df854-119">Эта функция всегда возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="df854-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="df854-120">В более ранних версиях приложения Visio эта функция отображается в виде _OPENFILE.</span><span class="sxs-lookup"><span data-stu-id="df854-120">In earlier versions of the Visio application, this function appears as _OPENFILE.</span></span> <span data-ttu-id="df854-121">Visio версии 4.0 и более поздних версий принимать любого из стилей.</span><span class="sxs-lookup"><span data-stu-id="df854-121">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="df854-122">Пример</span><span class="sxs-lookup"><span data-stu-id="df854-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="df854-123">Открывает указанный файл «MyFile.vsdx» в новом окне или активирует окно, если файл уже открыт.</span><span class="sxs-lookup"><span data-stu-id="df854-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

