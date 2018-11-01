---
title: Объект View (ADOX - ссылки для настольных баз данных Access)
TOCTitle: View Object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e1c3b2cc99cad4ba3b9ee71f0c44ee67b32d41d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873133"
---
# <a name="view-object-adox"></a><span data-ttu-id="5601f-102">Объект View (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5601f-102">View Object (ADOX)</span></span>


<span data-ttu-id="5601f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5601f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5601f-104">Представляет отфильтрованного набора записей или виртуальной таблицы.</span><span class="sxs-lookup"><span data-stu-id="5601f-104">Represents a filtered set of records or a virtual table.</span></span> <span data-ttu-id="5601f-105">При использовании в сочетании с объектом ADO [команду](command-object-ado.md) объект **View** можно использовать для Добавление, удаление или изменение представления.</span><span class="sxs-lookup"><span data-stu-id="5601f-105">When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="5601f-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="5601f-106">Remarks</span></span>

<span data-ttu-id="5601f-107">Представление — виртуальных таблицы, созданный из других баз данных таблицы или представления.</span><span class="sxs-lookup"><span data-stu-id="5601f-107">A view is a virtual table, created from other database tables or views.</span></span> <span data-ttu-id="5601f-108">Объект **View** позволяет создать представление без необходимости знать или используйте синтаксис поставщика «Создание ПРЕДСТАВЛЕНИЯ».</span><span class="sxs-lookup"><span data-stu-id="5601f-108">The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="5601f-109">Свойства объекта **представления** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5601f-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="5601f-110">Определение представления с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="5601f-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="5601f-111">Укажите объект ADO **команды** , который можно использовать для добавления, удаления или изменения представлений с помощью свойства [команды](command-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="5601f-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="5601f-112">Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="5601f-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

