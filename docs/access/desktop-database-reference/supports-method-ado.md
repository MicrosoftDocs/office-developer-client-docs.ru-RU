---
title: Supports Method (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61e6a4f3a5771c4d223380160204e4b0b350f210
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479792"
---
# <a name="supports-method-ado"></a><span data-ttu-id="f8ba5-102">Supports Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="f8ba5-102">Supports Method (ADO)</span></span>


<span data-ttu-id="f8ba5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8ba5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8ba5-104">Определяет, поддерживает ли указанный объект [набора записей](recordset-object-ado.md) определенного типа функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="f8ba5-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ba5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8ba5-105">Syntax</span></span>

<span data-ttu-id="f8ba5-106">*Логическое* = *набора записей*. Поддерживает (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="f8ba5-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="f8ba5-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8ba5-107">Return Value</span></span>

<span data-ttu-id="f8ba5-108">Возвращает **логическое** значение, указывающее, поддерживается ли все компоненты, определяемого аргументом *CursorOptions* поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f8ba5-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8ba5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8ba5-109">Parameters</span></span>

  - <span data-ttu-id="f8ba5-110">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="f8ba5-110">*CursorOptions*</span></span>

  - <span data-ttu-id="f8ba5-111">**Длинное** выражение, которое состоит из одного или нескольких значений [CursorOptionEnum](cursoroptionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ba5-111">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ba5-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="f8ba5-112">Remarks</span></span>

<span data-ttu-id="f8ba5-113">Используйте метод **поддерживает** , чтобы определить, какие функциональные возможности поддерживает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f8ba5-113">Use the **Supports** method to determine what types of functionality a **Recordset** object supports.</span></span> <span data-ttu-id="f8ba5-114">Если объект **набора записей** не поддерживают возможности, соответствующий константы находятся в *CursorOptions*, метод **поддерживает** возвращает **значение True**.</span><span class="sxs-lookup"><span data-stu-id="f8ba5-114">If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**.</span></span> <span data-ttu-id="f8ba5-115">В противном случае возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="f8ba5-115">Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f8ba5-116">Несмотря на то, что метод <STRONG>поддерживает</STRONG> может возвращать <STRONG>значение True</STRONG> для указанной функции, не гарантирует, что поставщик можно включить ни при каких обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="f8ba5-116">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</span></span> <span data-ttu-id="f8ba5-117">Метод <STRONG>поддерживает</STRONG> просто возвращает поставщик поддерживает ли эта функция, при условии определенных условий.</span><span class="sxs-lookup"><span data-stu-id="f8ba5-117">The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</span></span> <span data-ttu-id="f8ba5-118">Например метод <STRONG>поддерживает</STRONG> может указывать, что объект <STRONG>набора записей</STRONG> поддерживает обновления, даже если курсор основан на нескольких присоединиться к таблице, некоторые столбцы, не обновляются.</span><span class="sxs-lookup"><span data-stu-id="f8ba5-118">For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>


