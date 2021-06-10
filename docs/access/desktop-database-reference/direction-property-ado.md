---
title: Свойство Direction (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5885e89a3bce5d8b16ea855ce14689380655ad45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293870"
---
# <a name="direction-property-ado"></a><span data-ttu-id="877c5-102">Свойство Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="877c5-102">Direction property (ADO)</span></span>


<span data-ttu-id="877c5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="877c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="877c5-104">Указывает, является [](parameter-object-ado.md) ли параметр входным параметром, выходным параметром, входным и выходным параметром, или же параметр является возвращаемой величиной из сохраненной процедуры.</span><span class="sxs-lookup"><span data-stu-id="877c5-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="877c5-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="877c5-105">Settings and return values</span></span>

<span data-ttu-id="877c5-106">Задает или возвращает [значение ParameterDirectionEnum.](parameterdirectionenum.md)</span><span class="sxs-lookup"><span data-stu-id="877c5-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="877c5-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="877c5-107">Remarks</span></span>

<span data-ttu-id="877c5-108">Используйте свойство **Direction,** чтобы указать, как параметр передается в процедуру или из нее.</span><span class="sxs-lookup"><span data-stu-id="877c5-108">Use the **Direction** property to specify how a parameter is passed to or from a procedure.</span></span> <span data-ttu-id="877c5-109">Свойство **Direction** — чтение и написание; это позволяет работать с поставщиками, которые не возвращают эти сведения, или устанавливать эти сведения, если вам не нужно, чтобы ADO дополнительно вызывалась к поставщику для получения сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="877c5-109">The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="877c5-110">Не все поставщики могут определить направление параметров в сохраненных процедурах.</span><span class="sxs-lookup"><span data-stu-id="877c5-110">Not all providers can determine the direction of parameters in their stored procedures.</span></span> <span data-ttu-id="877c5-111">В этих случаях необходимо установить свойство **Direction** перед выполнением запроса.</span><span class="sxs-lookup"><span data-stu-id="877c5-111">In these cases, you must set the **Direction** property before you execute the query.</span></span>

