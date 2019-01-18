---
title: Оператор ТРАНЗАКЦИЙ (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705521"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="054c6-102">Оператор ТРАНЗАКЦИЙ (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="054c6-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="054c6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="054c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="054c6-104">Используется для начинать и завершать явные операции.</span><span class="sxs-lookup"><span data-stu-id="054c6-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="054c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="054c6-105">Syntax</span></span>

<span data-ttu-id="054c6-106">**Начало новой операции**:</span><span class="sxs-lookup"><span data-stu-id="054c6-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="054c6-107">НАЧАТЬ ТРАНЗАКЦИЮ</span><span class="sxs-lookup"><span data-stu-id="054c6-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="054c6-108">**Conclude транзакций с внесением всех рабочих выполнена во время операции**:</span><span class="sxs-lookup"><span data-stu-id="054c6-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="054c6-109">ФИКСАЦИЯ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="054c6-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="054c6-110">**Conclude транзакций с помощью отката все действия выполняются во время операции**:</span><span class="sxs-lookup"><span data-stu-id="054c6-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="054c6-111">ОТКАТ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="054c6-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="054c6-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="054c6-112">Remarks</span></span>

<span data-ttu-id="054c6-113">Не удалось автоматически запустить транзакции.</span><span class="sxs-lookup"><span data-stu-id="054c6-113">Transactions are not started automatically.</span></span> <span data-ttu-id="054c6-114">Чтобы запустить операцию, необходимо выполнить явно использовать команду НАЧАТЬ ТРАНЗАКЦИЙ.</span><span class="sxs-lookup"><span data-stu-id="054c6-114">To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="054c6-115">Операции могут быть вложенными до пяти уровней вложенности.</span><span class="sxs-lookup"><span data-stu-id="054c6-115">Transactions can be nested up to five levels deep.</span></span> <span data-ttu-id="054c6-116">Чтобы начать вложенных транзакций, используйте приступить к ТРАНЗАКЦИЙ в контексте существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="054c6-116">To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="054c6-117">Транзакции не поддерживаются для связанных таблиц.</span><span class="sxs-lookup"><span data-stu-id="054c6-117">Transactions are not supported for linked tables.</span></span>

