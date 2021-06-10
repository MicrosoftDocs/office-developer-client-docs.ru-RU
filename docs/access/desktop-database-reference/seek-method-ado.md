---
title: Поиск метода — ActiveX объектов данных (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308794"
---
# <a name="seek-method-ado"></a><span data-ttu-id="aa919-102">Поиск метода (ADO)</span><span class="sxs-lookup"><span data-stu-id="aa919-102">Seek method (ADO)</span></span>

<span data-ttu-id="aa919-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa919-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa919-104">Выполняется поиск индекса [наборов записей,](recordset-object-ado.md) чтобы быстро найти строку, которая соответствует указанным значениям, и изменить текущее положение строки в этой строке.</span><span class="sxs-lookup"><span data-stu-id="aa919-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa919-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa919-105">Syntax</span></span>

<span data-ttu-id="aa919-106">*набор записей.* Seek *KeyValues*, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="aa919-106">*recordset*.Seek *KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="aa919-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa919-107">Parameters</span></span>

|<span data-ttu-id="aa919-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="aa919-108">Parameter</span></span>|<span data-ttu-id="aa919-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aa919-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="aa919-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="aa919-110">*KeyValues*</span></span> |<span data-ttu-id="aa919-111">Массив **значений Variant.**</span><span class="sxs-lookup"><span data-stu-id="aa919-111">An array of **Variant** values.</span></span> <span data-ttu-id="aa919-112">Индекс состоит из одного или нескольких столбцов, а массив содержит значение для сравнения с каждым соответствующим столбцом.</span><span class="sxs-lookup"><span data-stu-id="aa919-112">An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="aa919-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="aa919-113">*SeekOption*</span></span> |<span data-ttu-id="aa919-114">Значение [SeekEnum,](seekenum.md) которое указывает тип сравнения между столбцами индекса и *соответствующими KeyValues.*</span><span class="sxs-lookup"><span data-stu-id="aa919-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="aa919-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa919-115">Remarks</span></span>

<span data-ttu-id="aa919-116">Используйте метод **Seek** совместно с свойством [Index,](index-property-ado.md) если поставщик поддерживает индексы на **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="aa919-116">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="aa919-117">Используйте метод Supports **(adSeek),** чтобы определить, поддерживает ли поставщик seek **и** метод [Supports](supports-method-ado.md) **(adIndex),** чтобы определить, поддерживает ли поставщик индексы.</span><span class="sxs-lookup"><span data-stu-id="aa919-117">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="aa919-118">(Например, поставщик [OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **Seek** and **Index.)**</span><span class="sxs-lookup"><span data-stu-id="aa919-118">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="aa919-119">Если **Seek** не находит нужную строку, ошибки не возникает, и строка находится в конце **recordset.**</span><span class="sxs-lookup"><span data-stu-id="aa919-119">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**.</span></span> <span data-ttu-id="aa919-120">Установите свойство **Index** в нужный индекс перед выполнением этого метода.</span><span class="sxs-lookup"><span data-stu-id="aa919-120">Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="aa919-121">Этот метод поддерживается только с помощью курсоров на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="aa919-121">This method is supported only with server-side cursors.</span></span> <span data-ttu-id="aa919-122">Поиск не поддерживается, когда значение [свойства CursorLocation](cursorlocation-property-ado.md) объекта **Recordset** **является adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="aa919-122">Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="aa919-123">Этот метод можно использовать только в том случае, если объект **Recordset** открыт со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect.**</span><span class="sxs-lookup"><span data-stu-id="aa919-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

