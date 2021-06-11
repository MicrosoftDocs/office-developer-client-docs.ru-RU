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
description: Указывает URL-адрес, имя файла или путь UNC, к которому необходимо перейти.
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438038"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="a3000-103">Address Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="a3000-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="a3000-104">Указывает URL-адрес, имя файла или путь UNC, к которому необходимо перейти.</span><span class="sxs-lookup"><span data-stu-id="a3000-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="a3000-105">Адрес можно указать как относительный путь на основе базового  пути, определенного  для документа в базовом окне Гиперссылка, на вкладке Сводка диалогового окна **Свойства** (щелкните вкладку **Файл,** щелкните **Info,** щелкните \*\* Свойства \*\*, а затем нажмите **кнопку Расширенные свойства**).</span><span class="sxs-lookup"><span data-stu-id="a3000-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="a3000-106">Если в документе нет базового пути, приложение перемещается по пути документа.</span><span class="sxs-lookup"><span data-stu-id="a3000-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="a3000-107">Если документ не сохранен, гиперссылка не установлена.</span><span class="sxs-lookup"><span data-stu-id="a3000-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3000-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3000-108">Remarks</span></span>

<span data-ttu-id="a3000-109">Вы также можете установить значение ячейки Address в диалоговом окне **Гиперссылки** (щелкните **Гиперссылку** на вкладке **Вставка).**</span><span class="sxs-lookup"><span data-stu-id="a3000-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="a3000-110">Чтобы получить ссылку на ячейку Address по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a3000-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3000-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a3000-111">Cell name:</span></span>  <br/> |<span data-ttu-id="a3000-112">Гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="a3000-112">Hyperlink.</span></span> <span data-ttu-id="a3000-113">*имя*  . Адрес, где гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="a3000-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="a3000-114">*имя*  строки гиперссылки</span><span class="sxs-lookup"><span data-stu-id="a3000-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="a3000-115">Чтобы получить ссылку на ячейку Address по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="a3000-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3000-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a3000-116">Section index:</span></span>  <br/> |<span data-ttu-id="a3000-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="a3000-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="a3000-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a3000-118">Row index:</span></span>  <br/> |<span data-ttu-id="a3000-119">**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="a3000-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a3000-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a3000-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a3000-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="a3000-121">**visHLinkAddress**</span></span> <br/> |
   

