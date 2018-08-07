---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807348"
---
# <a name="xlfgetname"></a><span data-ttu-id="63085-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="63085-104">xlfGetName</span></span>

<span data-ttu-id="63085-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="63085-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="63085-106">Возвращает определение: имя, как оно отображается в столбце **Формула** диалоговое окно **Диспетчер имен** , которая отображается при нажатии кнопки **Диспетчер имен** в разделе **Определенные имена** на вкладке " **формулы** ". Если определение содержит справочные материалы, они задаются в виде ссылок в стиле R1C1.</span><span class="sxs-lookup"><span data-stu-id="63085-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="63085-107">Используйте **xlfGetName** для проверки значения, определенные в имени.</span><span class="sxs-lookup"><span data-stu-id="63085-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="63085-108">Чтобы получить имя, соответствующее определение, используйте [xlfGetDef](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="63085-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="63085-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="63085-109">Parameters</span></span>

<span data-ttu-id="63085-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="63085-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="63085-111">Имя определяется на листе; Внешняя ссылка на имя, определенные на активной рабочей книги, `"!Sales"`; или внешним ссылку на имя, определенные для конкретного open книги, например, `"[Book1]SHEET1!Sales"`.</span><span class="sxs-lookup"><span data-stu-id="63085-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="63085-112">_pxNameText_ также может быть именем скрытым.</span><span class="sxs-lookup"><span data-stu-id="63085-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="63085-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="63085-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="63085-114">Указывает тип данных для возврата об имени.</span><span class="sxs-lookup"><span data-stu-id="63085-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="63085-115">Если **значение FALSE** или этот параметр опущен, возвращается определение.</span><span class="sxs-lookup"><span data-stu-id="63085-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="63085-116">Если **значение TRUE**, возвращает **значение TRUE,** Если имя определяется для только что листа, **значение FALSE** , если имя определяется для всей книги.</span><span class="sxs-lookup"><span data-stu-id="63085-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="63085-117">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63085-117">Property value/Return value</span></span>

<span data-ttu-id="63085-118">_pxRes_ (**xltypeStr**, **xltypeBool**или **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="63085-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="63085-119">В зависимости от того, значение, переданное для _pxInfoType_возвращает определение указанного имени (**xltypeStr**), или **значение TRUE** или **FALSE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="63085-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63085-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="63085-120">Remarks</span></span>

<span data-ttu-id="63085-121">Если флажок **Защитить лист и содержимое защищаемых ячеек** выбран в диалоговом окне " **Защитить лист** " для защиты книга, содержащая имя, **xlfGetName** возвращает `#N/A` значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="63085-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="63085-122">Чтобы просмотреть диалоговое окно " **Защитить лист** ", нажмите кнопку **Защитить лист** в разделе **изменения** на вкладке **Обзор** .</span><span class="sxs-lookup"><span data-stu-id="63085-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="63085-123">Ниже перечислены три примеры значений, возвращаемых вызовом **xlfGetDef** с аргументом указанного _pxNameText_ .</span><span class="sxs-lookup"><span data-stu-id="63085-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="63085-124">**Определения в Excel**</span><span class="sxs-lookup"><span data-stu-id="63085-124">**Definition in Excel**</span></span>|<span data-ttu-id="63085-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="63085-125">**_pxNameText_**</span></span>|<span data-ttu-id="63085-126">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="63085-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63085-127">Имя продаж на листе определяется как число 523.</span><span class="sxs-lookup"><span data-stu-id="63085-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="63085-128">«Продажи»</span><span class="sxs-lookup"><span data-stu-id="63085-128">"Sales"</span></span>  <br/> |<span data-ttu-id="63085-129">«= 523»</span><span class="sxs-lookup"><span data-stu-id="63085-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="63085-130">Имя прибыли на активном листе определяется как формулу = затраты на продажи.</span><span class="sxs-lookup"><span data-stu-id="63085-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="63085-131">"! Доход»</span><span class="sxs-lookup"><span data-stu-id="63085-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="63085-132">«= Затраты на продаж»</span><span class="sxs-lookup"><span data-stu-id="63085-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="63085-133">Имя базы данных на активном листе представляет собой диапазон A1:F500.</span><span class="sxs-lookup"><span data-stu-id="63085-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="63085-134">"! База данных»</span><span class="sxs-lookup"><span data-stu-id="63085-134">"!Database"</span></span>  <br/> |<span data-ttu-id="63085-135">«= R1C1:R500C6»</span><span class="sxs-lookup"><span data-stu-id="63085-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63085-136">См. также</span><span class="sxs-lookup"><span data-stu-id="63085-136">See also</span></span>

- [<span data-ttu-id="63085-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="63085-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="63085-138">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="63085-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

