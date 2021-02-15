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
# <a name="direction-property-ado"></a><span data-ttu-id="1f183-102">Свойство Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="1f183-102">Direction property (ADO)</span></span>


<span data-ttu-id="1f183-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f183-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f183-104">Указывает, представляет [](parameter-object-ado.md) ли параметр входной параметр, выходной параметр, входной и выходной параметр, а также является ли параметр возвращаемой величиной из хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="1f183-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1f183-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1f183-105">Settings and return values</span></span>

<span data-ttu-id="1f183-106">Задает или возвращает значение [ParameterDirectionEnum.](parameterdirectionenum.md)</span><span class="sxs-lookup"><span data-stu-id="1f183-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f183-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="1f183-107">Remarks</span></span>

<span data-ttu-id="1f183-108">Используйте свойство **Direction,** чтобы указать, как параметр передается процедуре или из нее.</span><span class="sxs-lookup"><span data-stu-id="1f183-108">Use the **Direction** property to specify how a parameter is passed to or from a procedure.</span></span> <span data-ttu-id="1f183-109">Свойство **Direction** имеет свойство read/write; Это позволяет работать с поставщиками, которые не возвращают эти сведения, или устанавливать эти сведения, если вы не хотите, чтобы ADO вызывался к поставщику для получения сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="1f183-109">The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="1f183-110">Не все поставщики могут определить направление параметров в хранимой процедуре.</span><span class="sxs-lookup"><span data-stu-id="1f183-110">Not all providers can determine the direction of parameters in their stored procedures.</span></span> <span data-ttu-id="1f183-111">В таких случаях перед выполнением запроса необходимо установить свойство **Direction.**</span><span class="sxs-lookup"><span data-stu-id="1f183-111">In these cases, you must set the **Direction** property before you execute the query.</span></span>

