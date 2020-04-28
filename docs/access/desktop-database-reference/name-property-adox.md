---
title: Свойство Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288653"
---
# <a name="name-property-adox"></a><span data-ttu-id="a2ebc-102">Свойство Name (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a2ebc-102">Name property (ADOX)</span></span>

<span data-ttu-id="a2ebc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2ebc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2ebc-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a2ebc-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a2ebc-105">Settings and return values</span></span>

<span data-ttu-id="a2ebc-106">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ebc-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2ebc-107">Remarks</span></span>

<span data-ttu-id="a2ebc-108">Имена не обязательно должны быть уникальными в пределах коллекции.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="a2ebc-109">Свойство **Name** доступно для чтения и записи в [столбцах](column-object-adox.md), [группах](group-object-adox.md), [ключах](key-object-adox.md), [индексе](index-object-adox.md), [таблице](table-object-adox.md)и [пользовательских](user-object-adox.md) объектах.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-109">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects.</span></span> <span data-ttu-id="a2ebc-110">Свойство **Name** доступно только для чтения в объектах [каталога](catalog-object-adox.md), [процедур](procedure-object-adox.md)и [представлений](view-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ebc-110">The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="a2ebc-111">Для объектов чтения и записи (**столбец**, **Группа**, **ключ**, **индекс**, **Таблица** и **пользовательские** объекты) значением по умолчанию является пустая строка ("").</span><span class="sxs-lookup"><span data-stu-id="a2ebc-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="a2ebc-112">Для ключей это свойство доступно только для чтения для объектов **Key** , уже добавленных в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-112">For keys, this property is read-only on **Key** objects already appended to a collection.</span></span>
> - <span data-ttu-id="a2ebc-113">Для таблиц это свойство доступно только для чтения для объектов **таблицы** , уже добавленных в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-113">For tables, this property is read-only for **Table** objects already appended to a collection.</span></span>


