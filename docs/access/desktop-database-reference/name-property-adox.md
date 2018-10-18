---
title: Name Property (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ea92fcca60d0c2877bf89359aac4532356a9874
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604052"
---
# <a name="name-property-adox"></a><span data-ttu-id="ced61-102">Name Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ced61-102">Name Property (ADOX)</span></span>


<span data-ttu-id="ced61-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ced61-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ced61-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ced61-104">Indicates the name of the object.</span></span>

<span data-ttu-id="ced61-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ced61-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="ced61-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ced61-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="ced61-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ced61-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="ced61-108">master</span><span class="sxs-lookup"><span data-stu-id="ced61-108">master</span></span>

<span data-ttu-id="ced61-109">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="ced61-109">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ced61-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="ced61-110">Remarks</span></span>

<span data-ttu-id="ced61-111">Имена не обязательно должно быть уникальным в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="ced61-111">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="ced61-112">Свойство **Name** — чтение и запись на [столбец](column-object-adox.md), [группы](group-object-adox.md), [ключа](key-object-adox.md), [индекса](index-object-adox.md), [таблицы](table-object-adox.md)и объектов- [пользователей](user-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="ced61-112">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects.</span></span> <span data-ttu-id="ced61-113">Свойство **Name** на объекты [каталога](catalog-object-adox.md), [процедуры](procedure-object-adox.md)и [представления](view-object-adox.md) только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ced61-113">The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="ced61-114">Для чтения и записи объектов (**столбец**, **группы**, **ключ**, **индекса**, **таблицы** и **пользователь** ), значение по умолчанию — пустая строка (»»).</span><span class="sxs-lookup"><span data-stu-id="ced61-114">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="ced61-115">Для клавиш это свойство соответствует на объекты <STRONG>ключ</STRONG> уже добавляется в конец коллекции только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ced61-115">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="ced61-116">Для таблиц это свойство доступно только для чтения для объектов <STRONG>в таблице</STRONG> , уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="ced61-116">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


