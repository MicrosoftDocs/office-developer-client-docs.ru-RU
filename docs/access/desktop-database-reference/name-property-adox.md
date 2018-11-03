---
title: Свойство Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a65bad49c7b9b7a7af91403b1119923b62daa04a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931248"
---
# <a name="name-property-adox"></a><span data-ttu-id="7e6c8-102">Свойство Name (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7e6c8-102">Name property (ADOX)</span></span>


<span data-ttu-id="7e6c8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e6c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e6c8-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7e6c8-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7e6c8-105">Settings and return values</span></span>

<span data-ttu-id="7e6c8-106">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e6c8-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e6c8-107">Remarks</span></span>

<span data-ttu-id="7e6c8-108">Имена не обязательно должно быть уникальным в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="7e6c8-109">Свойство **Name** — чтение и запись на [столбец](column-object-adox.md), [группы](group-object-adox.md), [ключа](key-object-adox.md), [индекса](index-object-adox.md), [таблицы](table-object-adox.md)и объектов- [пользователей](user-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7e6c8-109">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects.</span></span> <span data-ttu-id="7e6c8-110">Свойство **Name** на объекты [каталога](catalog-object-adox.md), [процедуры](procedure-object-adox.md)и [представления](view-object-adox.md) только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-110">The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="7e6c8-111">Для чтения и записи объектов (**столбец**, **группы**, **ключ**, **индекса**, **таблицы** и **пользователь** ), значение по умолчанию — пустая строка (»»).</span><span class="sxs-lookup"><span data-stu-id="7e6c8-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="7e6c8-112">Для клавиш это свойство соответствует на объекты <STRONG>ключ</STRONG> уже добавляется в конец коллекции только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-112">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="7e6c8-113">Для таблиц это свойство доступно только для чтения для объектов <STRONG>в таблице</STRONG> , уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="7e6c8-113">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


