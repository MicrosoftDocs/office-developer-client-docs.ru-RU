---
title: Метод Create (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718317"
---
# <a name="create-method-adox"></a><span data-ttu-id="d1e88-102">Метод Create (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d1e88-102">Create method (ADOX)</span></span>

<span data-ttu-id="d1e88-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1e88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1e88-104">Создает новый каталог.</span><span class="sxs-lookup"><span data-stu-id="d1e88-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1e88-105">Syntax</span></span>

<span data-ttu-id="d1e88-106">*Каталог*. Создание*стрсоедин*</span><span class="sxs-lookup"><span data-stu-id="d1e88-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="d1e88-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d1e88-107">Parameters</span></span>

|<span data-ttu-id="d1e88-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d1e88-108">Parameter</span></span>|<span data-ttu-id="d1e88-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d1e88-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d1e88-110">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="d1e88-110">*ConnectString*</span></span> |<span data-ttu-id="d1e88-111">**Строковое** значение, используемое для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="d1e88-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d1e88-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1e88-112">Remarks</span></span>

<span data-ttu-id="d1e88-113">Метод **Create** создает и открывает новый ADO [подключения](connection-object-ado.md) к источнику данных, указанной в *стрсоедин*.</span><span class="sxs-lookup"><span data-stu-id="d1e88-113">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*.</span></span> <span data-ttu-id="d1e88-114">В случае успешной свойству [ActiveConnection](activeconnection-property-adox.md) назначен новый объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="d1e88-114">If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="d1e88-115">Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="d1e88-115">An error will occur if the provider does not support creating new catalogs.</span></span>

