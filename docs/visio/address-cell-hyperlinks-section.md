---
title: Address Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Задает URL-адрес, имя файла или UNC-путь для перехода.
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338551"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="ed5a0-103">Address Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="ed5a0-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="ed5a0-104">Задает URL-адрес, имя файла или UNC-путь для перехода.</span><span class="sxs-lookup"><span data-stu-id="ed5a0-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="ed5a0-105">Вы можете указать адрес как относительный путь на основе базового пути, определенного для документа в поле **база** данных на вкладке **Сводка** диалогового окна **Свойства** (перейдите на вкладку **файл** , щелкните **сведения**, выберите \* \* Свойства \* \*. , а затем — **Дополнительные свойства**.</span><span class="sxs-lookup"><span data-stu-id="ed5a0-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="ed5a0-106">Если в документе нет базового пути, приложение переходит на основе пути документа.</span><span class="sxs-lookup"><span data-stu-id="ed5a0-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="ed5a0-107">Если документ не был сохранен, гиперссылка не определена.</span><span class="sxs-lookup"><span data-stu-id="ed5a0-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed5a0-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed5a0-108">Remarks</span></span>

<span data-ttu-id="ed5a0-109">Кроме того, можно задать значение ячейки адреса в диалоговом окне **гиперссылки** (щелкните гиперссылка на \*\*\*\* вкладке **Вставка** ).</span><span class="sxs-lookup"><span data-stu-id="ed5a0-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="ed5a0-110">Чтобы получить ссылку на ячейку Address по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ed5a0-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed5a0-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ed5a0-111">Cell name:</span></span>  <br/> |<span data-ttu-id="ed5a0-112">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="ed5a0-112">Hyperlink.</span></span> <span data-ttu-id="ed5a0-113">*Name (имя* ). Адрес гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="ed5a0-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="ed5a0-114">*Name* — имя строки гиперссылки</span><span class="sxs-lookup"><span data-stu-id="ed5a0-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="ed5a0-115">Чтобы получить ссылку на ячейку Address по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ed5a0-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed5a0-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ed5a0-116">Section index:</span></span>  <br/> |<span data-ttu-id="ed5a0-117">**Виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="ed5a0-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="ed5a0-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ed5a0-118">Row index:</span></span>  <br/> |<span data-ttu-id="ed5a0-119">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ed5a0-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ed5a0-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ed5a0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ed5a0-121">**Вишлинкаддресс**</span><span class="sxs-lookup"><span data-stu-id="ed5a0-121">**visHLinkAddress**</span></span> <br/> |
   

