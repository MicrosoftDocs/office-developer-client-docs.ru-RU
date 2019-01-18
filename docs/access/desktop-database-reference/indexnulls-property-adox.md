---
title: Свойство IndexNulls (ADOX)
TOCTitle: IndexNulls property (ADOX)
ms:assetid: 5c78c818-c23d-5b2c-d246-531aedc639df
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249326(v=office.15)
ms:contentKeyID: 48545089
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1419abb5dc66a59594284cf319487ef980bf62f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712885"
---
# <a name="indexnulls-property-adox"></a><span data-ttu-id="9ea34-102">Свойство IndexNulls (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9ea34-102">IndexNulls property (ADOX)</span></span>


<span data-ttu-id="9ea34-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ea34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ea34-104">Указывает, имеют ли записи, которые имеют значение null, значения в полях индекса записи индекса.</span><span class="sxs-lookup"><span data-stu-id="9ea34-104">Indicates whether records that have null values in their index fields have index entries.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9ea34-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9ea34-105">Settings and return values</span></span>

<span data-ttu-id="9ea34-106">Задает и возвращает значение [AllowNullsEnum](allownullsenum.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea34-106">Sets and returns an [AllowNullsEnum](allownullsenum.md) value.</span></span> <span data-ttu-id="9ea34-107">Значение по умолчанию — **adIndexNullsDisallow**.</span><span class="sxs-lookup"><span data-stu-id="9ea34-107">The default value is **adIndexNullsDisallow**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ea34-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ea34-108">Remarks</span></span>

<span data-ttu-id="9ea34-109">Это свойство доступно только для чтения объектов [индекса](index-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="9ea34-109">This property is read-only on [Index](index-object-adox.md) objects already appended to a collection.</span></span>

