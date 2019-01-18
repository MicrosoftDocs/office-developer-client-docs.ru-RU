---
title: Свойство NumericScale (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709056"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="1054d-102">Свойство NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1054d-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="1054d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1054d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1054d-104">Указывает масштаб числовое значение в столбце.</span><span class="sxs-lookup"><span data-stu-id="1054d-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1054d-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1054d-105">Settings and return values</span></span>

<span data-ttu-id="1054d-106">Задает и возвращает значение в **байтах** , масштаб значений данных в столбце, когда [Тип](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) свойства — **adNumeric** или **adDecimal**.</span><span class="sxs-lookup"><span data-stu-id="1054d-106">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**.</span></span> <span data-ttu-id="1054d-107">**NumericScale** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="1054d-107">**NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="1054d-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="1054d-108">Remarks</span></span>

<span data-ttu-id="1054d-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="1054d-109">The default value is zero (0).</span></span>

<span data-ttu-id="1054d-110">**NumericScale** доступен только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="1054d-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

