---
title: Свойство Database.Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9aecffc135ab402f02b8fd4e1cc234f4a6eb37d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927328"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="871bb-102">Свойство Database.Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="871bb-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="871bb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="871bb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="871bb-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="871bb-104">Syntax</span></span>

<span data-ttu-id="871bb-105">*выражение* . Подключение</span><span class="sxs-lookup"><span data-stu-id="871bb-105">*expression* .Connection</span></span>

<span data-ttu-id="871bb-106">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="871bb-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="871bb-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="871bb-107">Remarks</span></span>

<span data-ttu-id="871bb-108">Используйте свойство **подключение** для получения ссылки на объект **подключения** , соответствующее **базы данных**.</span><span class="sxs-lookup"><span data-stu-id="871bb-108">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**.</span></span> <span data-ttu-id="871bb-109">В DAO, объект **подключения** и его соответствующего объекта **базы данных** — это просто два разных объектных переменных ссылки на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="871bb-109">In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object.</span></span> <span data-ttu-id="871bb-110">**[База данных](connection-database-property-dao.md)** свойств объекта **подключения** и свойство **Connection** объекта **базы данных** облегчают изменять подключения к источнику данных ODBC с помощью ядро базы данных Microsoft Access, чтобы использовать технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="871bb-110">The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

