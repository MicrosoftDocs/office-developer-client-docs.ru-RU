---
title: Метод Delete (коллекция полей ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294108"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="4049e-102">Метод Delete (коллекция полей ADO)</span><span class="sxs-lookup"><span data-stu-id="4049e-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="4049e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4049e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="4049e-104">Удаляет объект из коллекции [Fields.](fields-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4049e-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4049e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4049e-105">Syntax</span></span>

<span data-ttu-id="4049e-106">*Поля*. Удаление *поля*</span><span class="sxs-lookup"><span data-stu-id="4049e-106">*Fields*.Delete *Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="4049e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4049e-107">Parameters</span></span>

|<span data-ttu-id="4049e-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4049e-108">Parameter</span></span>|<span data-ttu-id="4049e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4049e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4049e-110">*Field*</span><span class="sxs-lookup"><span data-stu-id="4049e-110">*Field*</span></span> |<span data-ttu-id="4049e-111">**Вариант,** который обозначает [удаляемый объект Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4049e-111">A **Variant** that designates the [Field](field-object-ado.md) object to delete.</span></span> <span data-ttu-id="4049e-112">Этот параметр может быть именем объекта **Field** или порядковой позицией самого **объекта Field.**</span><span class="sxs-lookup"><span data-stu-id="4049e-112">This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4049e-113">Заметки</span><span class="sxs-lookup"><span data-stu-id="4049e-113">Remarks</span></span>

<span data-ttu-id="4049e-114">Вызов метода **Fields.Delete** в открытом наборе [записей](recordset-object-ado.md) приводит к ошибке во время работы.</span><span class="sxs-lookup"><span data-stu-id="4049e-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

