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
# <a name="recordcount-property-ado"></a><span data-ttu-id="59053-102">Свойство RecordCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="59053-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="59053-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59053-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59053-104">Указывает количество записей в объекте [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="59053-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="59053-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59053-105">Return value</span></span>

<span data-ttu-id="59053-106">Возвращает значение **типа Long** , которое указывает количество записей в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="59053-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="59053-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="59053-107">Remarks</span></span>

<span data-ttu-id="59053-108">Используйте свойство **RecordCount** , чтобы узнать, сколько записей находится в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="59053-108">Use the **RecordCount** property to find out how many records are in a **Recordset** object.</span></span> <span data-ttu-id="59053-109">Свойство возвращает значение (1), если ADO не удается определить число записей или тип поставщика или курсора не поддерживает **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="59053-109">The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**.</span></span> <span data-ttu-id="59053-110">При чтении свойства **RecordCount** в закрытом **наборе записей** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="59053-110">Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="59053-111">Если объект **Recordset** поддерживает приблизительное позиционирование или закладки, то есть **поддерживает (Адаппрокспоситион)** или **поддерживает (адбукмарк)**, соответственно, возвращает **значение true** , это значение будет точным числом записей в **наборе**записей независимо от того, заполнено ли оно полностью.</span><span class="sxs-lookup"><span data-stu-id="59053-111">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated.</span></span> <span data-ttu-id="59053-112">Если объект **Recordset** не поддерживает приблизительное позиционирование, это свойство может быть значительным стоком ресурсов, так как все записи должны быть получены и учтены для возврата точного значения **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="59053-112">If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="59053-113">Тип курсора объекта **Recordset** влияет на то, можно ли определить количество записей.</span><span class="sxs-lookup"><span data-stu-id="59053-113">The cursor type of the **Recordset** object affects whether the number of records can be determined.</span></span> <span data-ttu-id="59053-114">Свойство **RecordCount** возвратит значение – 1 для однонаправленного курсора; фактическое количество для статического курсора или курсора набора ключей; и значение – 1 или фактическое количество динамического курсора, в зависимости от источника данных.</span><span class="sxs-lookup"><span data-stu-id="59053-114">The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

