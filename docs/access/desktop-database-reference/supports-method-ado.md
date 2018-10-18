---
title: Supports Method (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceeab22cda05738fdcec090acb5b4a2d6fc88a5b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604262"
---
# <a name="supports-method-ado"></a><span data-ttu-id="7516d-102">Supports Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="7516d-102">Supports Method (ADO)</span></span>


<span data-ttu-id="7516d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7516d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7516d-104">Определяет, поддерживает ли указанный объект [набора записей](recordset-object-ado.md) определенного типа функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="7516d-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="7516d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7516d-105">Syntax</span></span>

<span data-ttu-id="7516d-106">*Логическое* = *набора записей*. Поддерживает (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="7516d-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

<span data-ttu-id="7516d-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7516d-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="7516d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7516d-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="7516d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7516d-109">Return value</span></span>
>>>>>>> <span data-ttu-id="7516d-110">master</span><span class="sxs-lookup"><span data-stu-id="7516d-110">master</span></span>

<span data-ttu-id="7516d-111">Возвращает **логическое** значение, указывающее, поддерживается ли все компоненты, определяемого аргументом *CursorOptions* поставщиком.</span><span class="sxs-lookup"><span data-stu-id="7516d-111">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="7516d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7516d-112">Parameters</span></span>

  - <span data-ttu-id="7516d-113">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="7516d-113">*CursorOptions*</span></span>

  - <span data-ttu-id="7516d-114">**Длинное** выражение, которое состоит из одного или нескольких значений [CursorOptionEnum](cursoroptionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="7516d-114">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7516d-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="7516d-115">Remarks</span></span>

<span data-ttu-id="7516d-116">Используйте метод **поддерживает** , чтобы определить, какие функциональные возможности поддерживает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="7516d-116">Use the **Supports** method to determine what types of functionality a **Recordset** object supports.</span></span> <span data-ttu-id="7516d-117">Если объект **набора записей** не поддерживают возможности, соответствующий константы находятся в *CursorOptions*, метод **поддерживает** возвращает **значение True**.</span><span class="sxs-lookup"><span data-stu-id="7516d-117">If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**.</span></span> <span data-ttu-id="7516d-118">В противном случае возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="7516d-118">Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7516d-119">Несмотря на то, что метод <STRONG>поддерживает</STRONG> может возвращать <STRONG>значение True</STRONG> для указанной функции, не гарантирует, что поставщик можно включить ни при каких обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="7516d-119">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</span></span> <span data-ttu-id="7516d-120">Метод <STRONG>поддерживает</STRONG> просто возвращает поставщик поддерживает ли эта функция, при условии определенных условий.</span><span class="sxs-lookup"><span data-stu-id="7516d-120">The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</span></span> <span data-ttu-id="7516d-121">Например метод <STRONG>поддерживает</STRONG> может указывать, что объект <STRONG>набора записей</STRONG> поддерживает обновления, даже если курсор основан на нескольких присоединиться к таблице, некоторые столбцы, не обновляются.</span><span class="sxs-lookup"><span data-stu-id="7516d-121">For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>


