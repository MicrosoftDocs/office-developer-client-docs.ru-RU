---
title: Метод Supports (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703386"
---
# <a name="supports-method-ado"></a><span data-ttu-id="56d00-102">Метод Supports (ADO)</span><span class="sxs-lookup"><span data-stu-id="56d00-102">Supports method (ADO)</span></span>

<span data-ttu-id="56d00-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56d00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56d00-104">Определяет, поддерживает ли указанный объект [набора записей](recordset-object-ado.md) определенного типа функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="56d00-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d00-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56d00-105">Syntax</span></span>

<span data-ttu-id="56d00-106">*Логическое* = *набора записей*. Поддерживает (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="56d00-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="56d00-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56d00-107">Return value</span></span>

<span data-ttu-id="56d00-108">Возвращает **логическое** значение, указывающее, поддерживается ли все компоненты, определяемого аргументом *CursorOptions* поставщиком.</span><span class="sxs-lookup"><span data-stu-id="56d00-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="56d00-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="56d00-109">Parameters</span></span>

|<span data-ttu-id="56d00-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="56d00-110">Parameter</span></span>|<span data-ttu-id="56d00-111">Описание</span><span class="sxs-lookup"><span data-stu-id="56d00-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="56d00-112">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="56d00-112">*CursorOptions*</span></span> |<span data-ttu-id="56d00-113">**Длинное** выражение, которое состоит из одного или нескольких значений [CursorOptionEnum](cursoroptionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="56d00-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="56d00-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="56d00-114">Remarks</span></span>

<span data-ttu-id="56d00-115">Используйте метод **поддерживает** , чтобы определить, какие функциональные возможности поддерживает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="56d00-115">Use the **Supports** method to determine what types of functionality a **Recordset** object supports.</span></span> <span data-ttu-id="56d00-116">Если объект **набора записей** не поддерживают возможности, соответствующий константы находятся в *CursorOptions*, метод **поддерживает** возвращает **значение True**.</span><span class="sxs-lookup"><span data-stu-id="56d00-116">If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**.</span></span> <span data-ttu-id="56d00-117">В противном случае возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="56d00-117">Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="56d00-118">Несмотря на то, что метод **поддерживает** может возвращать **значение True** для указанной функции, не гарантирует, что поставщик можно включить ни при каких обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="56d00-118">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</span></span> <span data-ttu-id="56d00-119">Метод **поддерживает** просто возвращает поставщик поддерживает ли эта функция, при условии определенных условий.</span><span class="sxs-lookup"><span data-stu-id="56d00-119">The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</span></span> <span data-ttu-id="56d00-120">Например метод **поддерживает** может указывать, что объект **набора записей** поддерживает обновления, даже если курсор основан на нескольких присоединиться к таблице, некоторые столбцы, не обновляются.</span><span class="sxs-lookup"><span data-stu-id="56d00-120">For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>


