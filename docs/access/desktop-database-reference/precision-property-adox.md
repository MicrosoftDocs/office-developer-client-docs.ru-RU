---
title: Свойство Precision (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f05f6880a9599421189519f263cfb27bf1432325
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726164"
---
# <a name="precision-property-adox"></a><span data-ttu-id="481ba-102">Свойство Precision (ADOX)</span><span class="sxs-lookup"><span data-stu-id="481ba-102">Precision property (ADOX)</span></span>


<span data-ttu-id="481ba-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="481ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="481ba-104">Указывает максимальное точность значений данных в столбце.</span><span class="sxs-lookup"><span data-stu-id="481ba-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="481ba-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="481ba-105">Settings and return values</span></span>

<span data-ttu-id="481ba-106">Задает и возвращает значение типа **Long** , является максимальной точности значений данных в столбце, если свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) является числовым типом.</span><span class="sxs-lookup"><span data-stu-id="481ba-106">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is a numeric type.</span></span> <span data-ttu-id="481ba-107">**Точность** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="481ba-107">**Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="481ba-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="481ba-108">Remarks</span></span>

<span data-ttu-id="481ba-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="481ba-109">The default value is zero (0).</span></span>

<span data-ttu-id="481ba-110">Это свойство доступно только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="481ba-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

