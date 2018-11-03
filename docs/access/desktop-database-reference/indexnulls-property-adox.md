---
title: Свойство IndexNulls (ADOX)
TOCTitle: IndexNulls property (ADOX)
ms:assetid: 5c78c818-c23d-5b2c-d246-531aedc639df
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249326(v=office.15)
ms:contentKeyID: 48545089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a3aebecd1b93539a8e1cd8e37d7b9f0d81fdc6f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930639"
---
# <a name="indexnulls-property-adox"></a><span data-ttu-id="49a51-102">Свойство IndexNulls (ADOX)</span><span class="sxs-lookup"><span data-stu-id="49a51-102">IndexNulls property (ADOX)</span></span>


<span data-ttu-id="49a51-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49a51-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49a51-104">Указывает, имеют ли записи, которые имеют значение null, значения в полях индекса записи индекса.</span><span class="sxs-lookup"><span data-stu-id="49a51-104">Indicates whether records that have null values in their index fields have index entries.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="49a51-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="49a51-105">Settings and return values</span></span>

<span data-ttu-id="49a51-106">Задает и возвращает значение [AllowNullsEnum](allownullsenum.md) .</span><span class="sxs-lookup"><span data-stu-id="49a51-106">Sets and returns an [AllowNullsEnum](allownullsenum.md) value.</span></span> <span data-ttu-id="49a51-107">Значение по умолчанию — **adIndexNullsDisallow**.</span><span class="sxs-lookup"><span data-stu-id="49a51-107">The default value is **adIndexNullsDisallow**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a51-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="49a51-108">Remarks</span></span>

<span data-ttu-id="49a51-109">Это свойство доступно только для чтения объектов [индекса](index-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="49a51-109">This property is read-only on [Index](index-object-adox.md) objects already appended to a collection.</span></span>

