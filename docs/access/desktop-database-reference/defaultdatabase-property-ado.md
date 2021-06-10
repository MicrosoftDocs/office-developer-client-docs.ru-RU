---
title: Свойство DefaultDatabase (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294150"
---
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="cc568-102">Свойство DefaultDatabase (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc568-102">DefaultDatabase property (ADO)</span></span>


<span data-ttu-id="cc568-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc568-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc568-104">Указывает базу данных по умолчанию для объекта [Подключения.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="cc568-104">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cc568-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="cc568-105">Settings and return values</span></span>

<span data-ttu-id="cc568-106">Задает или возвращает значение **String,** которое оценивается с именем базы данных, доступной у поставщика.</span><span class="sxs-lookup"><span data-stu-id="cc568-106">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc568-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc568-107">Remarks</span></span>

<span data-ttu-id="cc568-108">Используйте свойство **DefaultDatabase** для настройки или возврата имени базы данных по умолчанию для определенного объекта **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="cc568-108">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="cc568-109">Если база данных существует по умолчанию, SQL строки могут использовать неквалифицированный синтаксис для доступа к объектам в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="cc568-109">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database.</span></span> <span data-ttu-id="cc568-110">Чтобы получить доступ к объектам в базе данных, не указанным в свойстве **DefaultDatabase,** необходимо квалифицировать имена объектов с нужным именем базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc568-110">To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name.</span></span> <span data-ttu-id="cc568-111">После подключения поставщик будет записывать данные базы данных по умолчанию в свойство **DefaultDatabase.**</span><span class="sxs-lookup"><span data-stu-id="cc568-111">Upon connection, the provider will write default database information to the **DefaultDatabase** property.</span></span> <span data-ttu-id="cc568-112">Некоторые поставщики позволяют только одну базу данных на подключение, в этом случае невозможно изменить свойство **DefaultDatabase.**</span><span class="sxs-lookup"><span data-stu-id="cc568-112">Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="cc568-113">Некоторые источники и поставщики данных могут не поддерживать эту функцию и могут возвращать ошибку или пустую строку.</span><span class="sxs-lookup"><span data-stu-id="cc568-113">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="cc568-114">**Удаленное использование службы данных** Это свойство не доступно для объекта клиентского **подключения.**</span><span class="sxs-lookup"><span data-stu-id="cc568-114">**Remote Data Service Usage** This property is not available on a client-side **Connection** object.</span></span>

