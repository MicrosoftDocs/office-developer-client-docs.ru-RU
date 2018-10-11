---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480570"
---
# <a name="connection-object-dao"></a><span data-ttu-id="42ec7-102">Connection Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="42ec7-102">Connection Object (DAO)</span></span>


<span data-ttu-id="42ec7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="42ec7-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="42ec7-104">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="42ec7-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="42ec7-105">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="42ec7-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>



<span data-ttu-id="42ec7-106">Объект **подключения** представляет подключение к базе данных ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="42ec7-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="42ec7-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="42ec7-107">Remarks</span></span>

<span data-ttu-id="42ec7-108">**Подключение** — это непостоянные объект, представляющий подключение к удаленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="42ec7-108">A **Connection** is a non-persistent object that represents a connection to a remote database.</span></span> <span data-ttu-id="42ec7-109">Объект **подключения** доступен только в рабочие области технология ODBCDirect (то есть, **рабочей области** объект, созданных с помощью параметра типа **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="42ec7-109">The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="42ec7-110">Код, написанный для более ранних версий DAO можно продолжить использование объекта <STRONG>базы данных</STRONG> для обеспечения обратной совместимости, но при желании новые возможности <STRONG>подключения</STRONG> , необходимо проверить код, чтобы использовать объект <STRONG>подключения</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="42ec7-110">Code written for earlier versions of DAO can continue to use the <STRONG>Database</STRONG> object for backward compatibility, but if the new features of a <STRONG>Connection</STRONG> are desired, you should revise code to use the <STRONG>Connection</STRONG> object.</span></span> <span data-ttu-id="42ec7-111">Чтобы упростить преобразование кода, можно получить ссылку на объект <STRONG>подключения</STRONG> из <STRONG>базы данных</STRONG> , прочитав статью свойство <A href="database-connection-property-dao.md">Connection</A> объекта <STRONG>базы данных</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="42ec7-111">To help with code conversion, you can obtain a <STRONG>Connection</STRONG> object reference from a <STRONG>Database</STRONG> by reading the <A href="database-connection-property-dao.md">Connection</A> property of the <STRONG>Database</STRONG> object.</span></span> <span data-ttu-id="42ec7-112">С другой стороны можно получить ссылку на объект <STRONG>базы данных</STRONG> из свойства объекта <STRONG>подключения к</STRONG> <STRONG>базе данных</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="42ec7-112">Conversely, you can obtain a <STRONG>Database</STRONG> object reference from the <STRONG>Connection</STRONG> object's <STRONG>Database</STRONG> property.</span></span></P>


