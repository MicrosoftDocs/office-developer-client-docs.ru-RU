---
title: Create Method (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482579"
---
# <a name="create-method-adox"></a><span data-ttu-id="a84b6-102">Create Method (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a84b6-102">Create Method (ADOX)</span></span>


<span data-ttu-id="a84b6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a84b6-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a84b6-104">Создает новый каталог.</span><span class="sxs-lookup"><span data-stu-id="a84b6-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="a84b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a84b6-105">Syntax</span></span>

<span data-ttu-id="a84b6-106">*Каталог*. Создание*стрсоедин*</span><span class="sxs-lookup"><span data-stu-id="a84b6-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="a84b6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a84b6-107">Parameters</span></span>

  - <span data-ttu-id="a84b6-108">*Стрсоедин*</span><span class="sxs-lookup"><span data-stu-id="a84b6-108">*ConnectString*</span></span>

  - <span data-ttu-id="a84b6-109">**Строковое** значение, используемое для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="a84b6-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="a84b6-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="a84b6-110">Remarks</span></span>

<span data-ttu-id="a84b6-111">Метод **Create** создает и открывает новый ADO [подключения](connection-object-ado.md) к источнику данных, указанной в *стрсоедин*.</span><span class="sxs-lookup"><span data-stu-id="a84b6-111">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*.</span></span> <span data-ttu-id="a84b6-112">В случае успешной свойству [ActiveConnection](activeconnection-property-adox.md) назначен новый объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a84b6-112">If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="a84b6-113">Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="a84b6-113">An error will occur if the provider does not support creating new catalogs.</span></span>

