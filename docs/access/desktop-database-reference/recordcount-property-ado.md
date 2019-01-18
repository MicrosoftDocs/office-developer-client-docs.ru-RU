---
title: Свойство RecordCount (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5ab01c419f703c1c17b1bf2b2cca2fb3844655d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712738"
---
# <a name="recordcount-property-ado"></a><span data-ttu-id="b2dcd-102">Свойство RecordCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="b2dcd-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="b2dcd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2dcd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2dcd-104">Указывает число записей в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b2dcd-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2dcd-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2dcd-105">Return value</span></span>

<span data-ttu-id="b2dcd-106">Возвращает значение типа **Long** , показывает, сколько записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="b2dcd-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2dcd-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="b2dcd-107">Remarks</span></span>

<span data-ttu-id="b2dcd-108">Используйте свойство **RecordCount** , чтобы узнать, сколько записей, в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b2dcd-108">Use the **RecordCount** property to find out how many records are in a **Recordset** object.</span></span> <span data-ttu-id="b2dcd-109">Это свойство возвращает значение -1 при ADO не может определить число записей, или если поставщик или тип курсора не поддерживает **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="b2dcd-109">The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**.</span></span> <span data-ttu-id="b2dcd-110">Чтение свойства **RecordCount** на закрытой **набора записей** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b2dcd-110">Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="b2dcd-111">Если объект **набора записей** поддерживает приблизительно, например расположение или закладки, то есть, **поддерживает (adApproxPosition)** или **поддерживает (adBookmark)**, соответственно, возвращает **значение True,** — это значение будет точное количество записей в \*\* Набор записей\*\*, независимо от того, является ли он полностью заполнен.</span><span class="sxs-lookup"><span data-stu-id="b2dcd-111">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated.</span></span> <span data-ttu-id="b2dcd-112">Если объект **набора записей** не поддерживает размещение приблизительно, например, это свойство возможно значительные затрат на ресурсы для всех записей необходимо получить и подсчитаны для возврата точное значение **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="b2dcd-112">If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="b2dcd-113">Тип текущей позиции объекта **набора записей** влияет можно определить число записей.</span><span class="sxs-lookup"><span data-stu-id="b2dcd-113">The cursor type of the **Recordset** object affects whether the number of records can be determined.</span></span> <span data-ttu-id="b2dcd-114">Свойство **RecordCount** возвращает значение -1 для курсора последовательного доступа; Фактическое количество для static или набора ключей курсора; и значение -1 или фактический количество для динамического курсора, в зависимости от источника данных.</span><span class="sxs-lookup"><span data-stu-id="b2dcd-114">The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

