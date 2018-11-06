---
title: Свойство Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c66c4e6b8fc43a27b2feb87e45ec436e3abfa49
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998919"
---
# <a name="name-property-adox"></a><span data-ttu-id="7b11d-102">Свойство Name (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7b11d-102">Name property (ADOX)</span></span>

<span data-ttu-id="7b11d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b11d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b11d-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7b11d-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7b11d-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7b11d-105">Settings and return values</span></span>

<span data-ttu-id="7b11d-106">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="7b11d-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b11d-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b11d-107">Remarks</span></span>

<span data-ttu-id="7b11d-108">Имена не обязательно должно быть уникальным в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="7b11d-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="7b11d-109">Свойство **Name** — чтение и запись на [столбец](column-object-adox.md), [группы](group-object-adox.md), [ключа](key-object-adox.md), [индекса](index-object-adox.md), [таблицы](table-object-adox.md)и объектов- [пользователей](user-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7b11d-109">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects.</span></span> <span data-ttu-id="7b11d-110">Свойство **Name** на объекты [каталога](catalog-object-adox.md), [процедуры](procedure-object-adox.md)и [представления](view-object-adox.md) только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7b11d-110">The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="7b11d-111">Для чтения и записи объектов (**столбец**, **группы**, **ключ**, **индекса**, **таблицы** и **пользователь** ), значение по умолчанию — пустая строка (»»).</span><span class="sxs-lookup"><span data-stu-id="7b11d-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="7b11d-112">Для клавиш это свойство соответствует на объекты **ключ** уже добавляется в конец коллекции только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7b11d-112">For keys, this property is read-only on **Key** objects already appended to a collection.</span></span>
> - <span data-ttu-id="7b11d-113">Для таблиц это свойство доступно только для чтения для объектов **в таблице** , уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="7b11d-113">For tables, this property is read-only for **Table** objects already appended to a collection.</span></span>


