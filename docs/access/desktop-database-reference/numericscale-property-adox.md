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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288520"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="0369d-102">Свойство NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0369d-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="0369d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0369d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0369d-104">Указывает масштаб числимого значения в столбце.</span><span class="sxs-lookup"><span data-stu-id="0369d-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0369d-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0369d-105">Settings and return values</span></span>

<span data-ttu-id="0369d-106">Задает и возвращает значение **byte,** которое является масштабом значений данных в столбце, если свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) является **adNumeric** или **adDecimal**.</span><span class="sxs-lookup"><span data-stu-id="0369d-106">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**.</span></span> <span data-ttu-id="0369d-107">**NumericScale** игнорируется для всех других типов данных.</span><span class="sxs-lookup"><span data-stu-id="0369d-107">**NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="0369d-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="0369d-108">Remarks</span></span>

<span data-ttu-id="0369d-109">Значение по умолчанию — ноль (0).</span><span class="sxs-lookup"><span data-stu-id="0369d-109">The default value is zero (0).</span></span>

<span data-ttu-id="0369d-110">**NumericScale** доступно только для чтения для объектов [Column,](column-object-adox.md) которые уже были приданы к коллекции.</span><span class="sxs-lookup"><span data-stu-id="0369d-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

