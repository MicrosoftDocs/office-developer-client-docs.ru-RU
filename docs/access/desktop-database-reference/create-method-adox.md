---
title: Метод Create (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 866faae5d8c99258075a81f504fa9ce069f4690a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949378"
---
# <a name="create-method-adox"></a><span data-ttu-id="7eef0-102">Метод Create (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7eef0-102">Create method (ADOX)</span></span>

<span data-ttu-id="7eef0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7eef0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7eef0-104">Создает новый каталог.</span><span class="sxs-lookup"><span data-stu-id="7eef0-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eef0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7eef0-105">Syntax</span></span>

<span data-ttu-id="7eef0-106">*Каталог*. Создание*стрсоедин*</span><span class="sxs-lookup"><span data-stu-id="7eef0-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="7eef0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7eef0-107">Parameters</span></span>

|<span data-ttu-id="7eef0-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="7eef0-108">Parameter</span></span>|<span data-ttu-id="7eef0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7eef0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7eef0-110">*Стрсоедин*</span><span class="sxs-lookup"><span data-stu-id="7eef0-110">*ConnectString*</span></span> |<span data-ttu-id="7eef0-111">**Строковое** значение, используемое для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="7eef0-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7eef0-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="7eef0-112">Remarks</span></span>

<span data-ttu-id="7eef0-113">Метод **Create** создает и открывает новый ADO [подключения](connection-object-ado.md) к источнику данных, указанной в *стрсоедин*.</span><span class="sxs-lookup"><span data-stu-id="7eef0-113">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*.</span></span> <span data-ttu-id="7eef0-114">В случае успешной свойству [ActiveConnection](activeconnection-property-adox.md) назначен новый объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="7eef0-114">If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="7eef0-115">Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7eef0-115">An error will occur if the provider does not support creating new catalogs.</span></span>

