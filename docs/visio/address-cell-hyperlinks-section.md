---
title: Ячейка Address (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Указывает URL-адрес, имя файла или UNC-путь к которой необходимо перейти.
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813157"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="295c6-103">Ячейка Address (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="295c6-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="295c6-104">Указывает URL-адрес, имя файла или UNC-путь к которой необходимо перейти.</span><span class="sxs-lookup"><span data-stu-id="295c6-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="295c6-105">Можно указать адрес как относительный путь на основе базового пути, определенных для документов в поле **База гиперссылки** на вкладке **Сводка** диалогового окна **Свойства** (перейдите на вкладку **файл** , щелкните **информация**, нажмите кнопку ** Свойства ** и выберите команду **Дополнительные свойства**).</span><span class="sxs-lookup"><span data-stu-id="295c6-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click ** Properties **, and then click **Advanced Properties**).</span></span> <span data-ttu-id="295c6-106">Если в документе есть путь не базового, приложение переходит на основе на путь к документу.</span><span class="sxs-lookup"><span data-stu-id="295c6-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="295c6-107">Если документ не был сохранен, гиперссылки не определено.</span><span class="sxs-lookup"><span data-stu-id="295c6-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="295c6-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="295c6-108">Remarks</span></span>

<span data-ttu-id="295c6-109">Можно также задать значение ячейки адреса в диалоговом окне **гиперссылки** (щелкните **гиперссылку** на вкладке **Вставка** ).</span><span class="sxs-lookup"><span data-stu-id="295c6-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="295c6-110">Для получения ссылки на ячейки адрес по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="295c6-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="295c6-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="295c6-111">Cell name:</span></span>  <br/> |<span data-ttu-id="295c6-112">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="295c6-112">Hyperlink.</span></span> <span data-ttu-id="295c6-113">*имя* . Адрес where гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="295c6-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="295c6-114">*имя* — это имя строки гиперссылки</span><span class="sxs-lookup"><span data-stu-id="295c6-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="295c6-115">Чтобы получить ссылку на адрес ячейки по имени из другой формулы или из программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="295c6-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="295c6-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="295c6-116">Section index:</span></span>  <br/> |<span data-ttu-id="295c6-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="295c6-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="295c6-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="295c6-118">Row index:</span></span>  <br/> |<span data-ttu-id="295c6-119">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="295c6-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="295c6-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="295c6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="295c6-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="295c6-121">**visHLinkAddress**</span></span> <br/> |
   

