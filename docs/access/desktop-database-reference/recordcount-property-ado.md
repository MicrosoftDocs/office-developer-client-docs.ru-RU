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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300772"
---
# <a name="recordcount-property-ado"></a><span data-ttu-id="fc4a3-102">Свойство RecordCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc4a3-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="fc4a3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc4a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc4a3-104">Указывает количество записей в [объекте Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="fc4a3-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc4a3-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc4a3-105">Return value</span></span>

<span data-ttu-id="fc4a3-106">Возвращает **длинное** значение, которое указывает количество записей в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="fc4a3-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc4a3-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="fc4a3-107">Remarks</span></span>

<span data-ttu-id="fc4a3-108">Чтобы узнать, сколько записей находится в объекте **Recordset,** используйте свойство **RecordCount.**</span><span class="sxs-lookup"><span data-stu-id="fc4a3-108">Use the **RecordCount** property to find out how many records are in a **Recordset** object.</span></span> <span data-ttu-id="fc4a3-109">Свойство возвращает -1, когда ADO не может определить количество записей или если поставщик или тип курсора не поддерживает **RecordCount.**</span><span class="sxs-lookup"><span data-stu-id="fc4a3-109">The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**.</span></span> <span data-ttu-id="fc4a3-110">Чтение свойства **RecordCount** в закрытом **наборе записей** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-110">Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="fc4a3-111">Если объект **Recordset** поддерживает приблизительное расположение или закладки , то есть поддерживает **(adApproxPosition)** или **Supports (adBookmark)** соответственно, возвращает Значение **True** — это значение будет точным числом записей в Наборе записей **независимо** от того, был ли он заполнен полностью.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-111">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated.</span></span> <span data-ttu-id="fc4a3-112">Если объект **Recordset** не поддерживает приблизительное позиционирование, это свойство может быть значительным сливом ресурсов, так как для возврата точного значения **RecordCount** необходимо извлечь и пересчитать все записи.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-112">If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="fc4a3-113">Тип курсора объекта **Recordset** влияет на то, можно ли определить количество записей.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-113">The cursor type of the **Recordset** object affects whether the number of records can be determined.</span></span> <span data-ttu-id="fc4a3-114">Свойство **RecordCount** возвращает -1 для курсора только вперед; фактическое количество для статического курсора или курсора наборов ключей; и либо -1, либо фактическое число динамических курсоров в зависимости от источника данных.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-114">The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

