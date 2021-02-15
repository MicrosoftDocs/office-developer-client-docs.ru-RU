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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291478"
---
# <a name="indexnulls-property-adox"></a><span data-ttu-id="417f4-102">Свойство IndexNulls (ADOX)</span><span class="sxs-lookup"><span data-stu-id="417f4-102">IndexNulls property (ADOX)</span></span>


<span data-ttu-id="417f4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="417f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="417f4-104">Указывает, имеют ли записи, которые имеют значения null в своих полях индекса.</span><span class="sxs-lookup"><span data-stu-id="417f4-104">Indicates whether records that have null values in their index fields have index entries.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="417f4-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="417f4-105">Settings and return values</span></span>

<span data-ttu-id="417f4-106">Задает и возвращает значение [AllowNullsEnum.](allownullsenum.md)</span><span class="sxs-lookup"><span data-stu-id="417f4-106">Sets and returns an [AllowNullsEnum](allownullsenum.md) value.</span></span> <span data-ttu-id="417f4-107">Значение по умолчанию **— adIndexNullsDisallow.**</span><span class="sxs-lookup"><span data-stu-id="417f4-107">The default value is **adIndexNullsDisallow**.</span></span>

## <a name="remarks"></a><span data-ttu-id="417f4-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="417f4-108">Remarks</span></span>

<span data-ttu-id="417f4-109">Это свойство доступно только для чтения в [объектах Index,](index-object-adox.md) которые уже были appended в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="417f4-109">This property is read-only on [Index](index-object-adox.md) objects already appended to a collection.</span></span>

