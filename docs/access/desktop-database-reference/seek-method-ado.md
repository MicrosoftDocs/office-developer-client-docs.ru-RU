---
title: Способа - ActiveX Data Objects (ADO)
TOCTitle: Seek Method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c4ad4376eb50c9eeec0efa6db0c0e9446cd0860
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482529"
---
# <a name="seek-method-ado"></a><span data-ttu-id="f353a-102">Seek Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="f353a-102">Seek Method (ADO)</span></span>


<span data-ttu-id="f353a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f353a-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="f353a-104">Выполняет поиск индекса [набора записей](recordset-object-ado.md) для быстрого поиска строку, в которой совпадает с указанными значениями и изменяет текущее положение строки на эту строку.</span><span class="sxs-lookup"><span data-stu-id="f353a-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="f353a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f353a-105">Syntax</span></span>

<span data-ttu-id="f353a-106">*набор записей*. Поиск*KeyValues*, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="f353a-106">*recordset*.Seek*KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="f353a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f353a-107">Parameters</span></span>

  - <span data-ttu-id="f353a-108">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="f353a-108">*KeyValues*</span></span>

  - <span data-ttu-id="f353a-109">Массив значений **Variant** .</span><span class="sxs-lookup"><span data-stu-id="f353a-109">An array of **Variant** values.</span></span> <span data-ttu-id="f353a-110">Индекс состоит из одного или нескольких столбцов и массив содержит значение, которое будет сравниваться с все соответствующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="f353a-110">An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>

  - <span data-ttu-id="f353a-111">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="f353a-111">*SeekOption*</span></span>

  - <span data-ttu-id="f353a-112">[SeekEnum](seekenum.md) значение, задающее тип сравнения между столбцов индекса и соответствующие *KeyValues*.</span><span class="sxs-lookup"><span data-stu-id="f353a-112">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>

## <a name="remarks"></a><span data-ttu-id="f353a-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="f353a-113">Remarks</span></span>

<span data-ttu-id="f353a-114">Используйте метод **Seek** в сочетании со свойством [индекса](index-property-ado.md) , если базовый поставщик поддерживает индексы в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f353a-114">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="f353a-115">Используйте метод [поддерживает](supports-method-ado.md)**(adSeek)** , чтобы определить, поддерживает ли основного поставщика **поиска**и метод **Supports(adIndex)** , чтобы определить, поддерживает ли поставщик индексов.</span><span class="sxs-lookup"><span data-stu-id="f353a-115">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="f353a-116">(Например, [Поставщик OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **поиска** и **индекса**).</span><span class="sxs-lookup"><span data-stu-id="f353a-116">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="f353a-117">Если **Поиск** не удается найти нужную строку, ошибка не происходит и размещенный строку в конец **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="f353a-117">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**.</span></span> <span data-ttu-id="f353a-118">Значение свойства **Index** желаемую индекса перед выполнением этого метода.</span><span class="sxs-lookup"><span data-stu-id="f353a-118">Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="f353a-119">Этот метод поддерживается только записей на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="f353a-119">This method is supported only with server-side cursors.</span></span> <span data-ttu-id="f353a-120">Поиск не поддерживается, если значение свойства [CursorLocation](cursorlocation-property-ado.md) объекта **набора записей** является **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="f353a-120">Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="f353a-121">Этот метод можно использовать, только когда со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect**был открыт в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f353a-121">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

