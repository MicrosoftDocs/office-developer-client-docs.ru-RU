---
title: View Object (ADOX — ссылка на базу данных для настольных компьютеров)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306051"
---
# <a name="view-object-adox"></a><span data-ttu-id="dd63e-102">Просмотр объекта (ADOX)</span><span class="sxs-lookup"><span data-stu-id="dd63e-102">View object (ADOX)</span></span>


<span data-ttu-id="dd63e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd63e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd63e-104">Представляет фильтрованный набор записей или виртуальную таблицу.</span><span class="sxs-lookup"><span data-stu-id="dd63e-104">Represents a filtered set of records or a virtual table.</span></span> <span data-ttu-id="dd63e-105">При использовании в сочетании с объектом ADO [Command](command-object-ado.md) объект **View** можно использовать для добавления, удаления или изменения представлений.</span><span class="sxs-lookup"><span data-stu-id="dd63e-105">When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd63e-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="dd63e-106">Remarks</span></span>

<span data-ttu-id="dd63e-107">Представление — это виртуальная таблица, созданная из других таблиц или представлений баз данных.</span><span class="sxs-lookup"><span data-stu-id="dd63e-107">A view is a virtual table, created from other database tables or views.</span></span> <span data-ttu-id="dd63e-108">Объект **View** позволяет создавать представление без необходимости знать синтаксис "CREATE VIEW" поставщика или использовать его.</span><span class="sxs-lookup"><span data-stu-id="dd63e-108">The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="dd63e-109">Со свойствами объекта **View** можно:</span><span class="sxs-lookup"><span data-stu-id="dd63e-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="dd63e-110">Определите представление с [свойством Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="dd63e-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="dd63e-111">Укажите объект ADO **Command,** который можно использовать для добавления, удаления или изменения представлений с помощью [свойства Command.](command-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="dd63e-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="dd63e-112">Сведения о дате возврата со свойствами [DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="dd63e-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

