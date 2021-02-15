---
title: Supports method (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308465"
---
# <a name="supports-method-ado"></a><span data-ttu-id="37fbb-102">Supports method (ADO)</span><span class="sxs-lookup"><span data-stu-id="37fbb-102">Supports method (ADO)</span></span>

<span data-ttu-id="37fbb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37fbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37fbb-104">Определяет, поддерживает ли указанный [объект Recordset](recordset-object-ado.md) определенный тип функций.</span><span class="sxs-lookup"><span data-stu-id="37fbb-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="37fbb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37fbb-105">Syntax</span></span>

<span data-ttu-id="37fbb-106">*boolean*  =  *recordset*. Supports *(CursorOptions)*</span><span class="sxs-lookup"><span data-stu-id="37fbb-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="37fbb-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37fbb-107">Return value</span></span>

<span data-ttu-id="37fbb-108">Возвращает значение **boolean,** которое указывает, поддерживаются ли поставщиком все функции, указанные аргументом *CursorOptions.*</span><span class="sxs-lookup"><span data-stu-id="37fbb-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="37fbb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="37fbb-109">Parameters</span></span>

|<span data-ttu-id="37fbb-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="37fbb-110">Parameter</span></span>|<span data-ttu-id="37fbb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="37fbb-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="37fbb-112">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="37fbb-112">*CursorOptions*</span></span> |<span data-ttu-id="37fbb-113">**Длинное** выражение, состоящее из одного или нескольких значений [CursorOptionEnum.](cursoroptionenum.md)</span><span class="sxs-lookup"><span data-stu-id="37fbb-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="37fbb-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="37fbb-114">Remarks</span></span>

<span data-ttu-id="37fbb-115">Используйте метод **Supports,** чтобы определить, какие типы функций поддерживает объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="37fbb-115">Use the **Supports** method to determine what types of functionality a **Recordset** object supports.</span></span> <span data-ttu-id="37fbb-116">Если объект **Recordset поддерживает** функции, соответствующие константы которых находятся в *cursorOptions,* метод **Supports** возвращает **true**.</span><span class="sxs-lookup"><span data-stu-id="37fbb-116">If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**.</span></span> <span data-ttu-id="37fbb-117">В противном случае возвращается **false.**</span><span class="sxs-lookup"><span data-stu-id="37fbb-117">Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="37fbb-118">Хотя метод **Supports** может возвращать **true** для заданной функции, он не гарантирует, что поставщик сможет сделать эту функцию доступной при любых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="37fbb-118">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</span></span> <span data-ttu-id="37fbb-119">Метод **Supports** просто возвращает, может ли поставщик поддерживать указанные функции при условии, что выполнены определенные условия.</span><span class="sxs-lookup"><span data-stu-id="37fbb-119">The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</span></span> <span data-ttu-id="37fbb-120">Например, метод **Supports** может указывать на то, что объект **Recordset** поддерживает обновления, даже если курсор основан на нескольких скомплексе таблиц, некоторые столбцы которых не поддерживают обновление.</span><span class="sxs-lookup"><span data-stu-id="37fbb-120">For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>


