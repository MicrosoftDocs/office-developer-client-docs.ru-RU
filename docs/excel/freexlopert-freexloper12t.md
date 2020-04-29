---
title: FreeXLOperT/FreeXLOper12T
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FreeXLOper12T
- FreeXLOperT
keywords:
- Функция фрикслоперт [Excel 2007], функция FreeXLOper12T [Excel 2007]
localization_priority: Normal
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0b604cbe5cb24ac7d8de28278dfbcf0d4fd92c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421524"
---
# <a name="freexlopertfreexloper12t"></a><span data-ttu-id="fe852-104">FreeXLOperT/FreeXLOper12T</span><span class="sxs-lookup"><span data-stu-id="fe852-104">FreeXLOperT/FreeXLOper12T</span></span>

 <span data-ttu-id="fe852-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fe852-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fe852-106">Функция Framework, которая освобождает память, связанную с **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="fe852-106">Framework function that frees memory associated with an **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="fe852-107">Функция предполагает, что память была выделена с помощью вызовов malloc в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="fe852-107">The function assumes that the memory was allocated with calls to malloc within the DLL.</span></span> <span data-ttu-id="fe852-108">Если память была выделена Microsoft Excel или другим способом или каким бы то ни было другим процессом, эта функция не должна использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="fe852-108">If the memory was allocated by Microsoft Excel or in some other way or by some other process, this function should not be used to free the memory.</span></span> <span data-ttu-id="fe852-109">Используйте [кслфри](xlfree.md) для освобождения памяти, выделенной Excel для **XLOPER**/ **, с.**</span><span class="sxs-lookup"><span data-stu-id="fe852-109">Use [xlFree](xlfree.md) to free memory allocated by Excel for **XLOPER**/ **XLOPER12**s.</span></span> 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="fe852-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe852-110">Parameters</span></span>

 <span data-ttu-id="fe852-111">_пкслопер_ (**лпкслопер**)</span><span class="sxs-lookup"><span data-stu-id="fe852-111">_pxloper_ (**LPXLOPER**)</span></span>
  
 <span data-ttu-id="fe852-112">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="fe852-112">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="fe852-113">Указатель на значение параметра **XLOPER**/ **XLOPER12** , которое нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="fe852-113">Pointer to the **XLOPER**/ **XLOPER12** to be freed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fe852-114">Пример</span><span class="sxs-lookup"><span data-stu-id="fe852-114">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
void FreeXLOper12T(LPXLOPER12 pxloper12)
{
   DWORD xltype;
   int cxloper12;
   LPXLOPER12 pxloper12Free;
   xltype = pxloper12->xltype;
   switch (xltype)
   {
   case xltypeStr:
      if (pxloper12->val.str != NULL)
         free(pxloper12->val.str);
      break;
   case xltypeRef:
      if (pxloper12->val.mref.lpmref != NULL)
         free(pxloper12->val.mref.lpmref);
      break;
   case xltypeMulti:
      cxloper12 = pxloper12->val.array.rows * pxloper12->val.array.columns;
      if (pxloper12->val.array.lparray)
      {
         pxloper12Free = pxloper12->val.array.lparray;
         while (cxloper12 > 0)
         {
            FreeXLOper12T(pxloper12Free);
            pxloper12Free++;
            cxloper12--;
         }
         free(pxloper12->val.array.lparray);
      }
      break;
   case xltypeBigData:
      if (pxloper12->val.bigdata.h.lpbData != NULL)
         free(pxloper12->val.bigdata.h.lpbData);
      break;
   }
}
```

## <a name="see-also"></a><span data-ttu-id="fe852-115">См. также</span><span class="sxs-lookup"><span data-stu-id="fe852-115">See also</span></span>



[<span data-ttu-id="fe852-116">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="fe852-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

