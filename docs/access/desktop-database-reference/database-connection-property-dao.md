---
title: Свойство Database. Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77d9bfa30dbfab21fd75de36b336a25e6af3187e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294997"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="24486-102">Свойство Database. Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="24486-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="24486-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24486-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="24486-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24486-104">Syntax</span></span>

<span data-ttu-id="24486-105">*Expression* . Соединений</span><span class="sxs-lookup"><span data-stu-id="24486-105">*expression* .Connection</span></span>

<span data-ttu-id="24486-106">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="24486-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24486-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="24486-107">Remarks</span></span>

<span data-ttu-id="24486-108">Используйте свойство **Connection** для получения ссылки на объект **подключения** , соответствующий **базе данных**.</span><span class="sxs-lookup"><span data-stu-id="24486-108">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**.</span></span> <span data-ttu-id="24486-109">В DAO объект **Connection** и соответствующий ему объект **Database** — это просто две разных ссылки на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="24486-109">In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object.</span></span> <span data-ttu-id="24486-110">Свойство **[Database](connection-database-property-dao.md)** объекта **Connection** и свойство **Connection** объекта **Database** упрощают изменение подключений к источнику данных ODBC с помощью ядра СУБД Microsoft Access для использования ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="24486-110">The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

