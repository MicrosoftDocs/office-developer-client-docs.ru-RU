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
ms.openlocfilehash: 6d93fc90beded30d96b4db54c35ab3046da06899
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862668"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="dc6d1-102">Оператор ТРАНЗАКЦИЙ (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="dc6d1-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="dc6d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc6d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dc6d1-104">Используется для начинать и завершать явные операции.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc6d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc6d1-105">Syntax</span></span>

<span data-ttu-id="dc6d1-106">**Начало новой операции**:</span><span class="sxs-lookup"><span data-stu-id="dc6d1-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="dc6d1-107">НАЧАТЬ ТРАНЗАКЦИЮ</span><span class="sxs-lookup"><span data-stu-id="dc6d1-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="dc6d1-108">**Conclude транзакций с внесением всех рабочих выполнена во время операции**:</span><span class="sxs-lookup"><span data-stu-id="dc6d1-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="dc6d1-109">ФИКСАЦИЯ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="dc6d1-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="dc6d1-110">**Conclude транзакций с помощью отката все действия выполняются во время операции**:</span><span class="sxs-lookup"><span data-stu-id="dc6d1-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="dc6d1-111">ОТКАТ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="dc6d1-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="dc6d1-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc6d1-112">Remarks</span></span>

<span data-ttu-id="dc6d1-113">Не удалось автоматически запустить транзакции.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-113">Transactions are not started automatically.</span></span> <span data-ttu-id="dc6d1-114">Чтобы запустить операцию, необходимо выполнить явно использовать команду НАЧАТЬ ТРАНЗАКЦИЙ.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-114">To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="dc6d1-115">Операции могут быть вложенными до пяти уровней вложенности.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-115">Transactions can be nested up to five levels deep.</span></span> <span data-ttu-id="dc6d1-116">Чтобы начать вложенных транзакций, используйте приступить к ТРАНЗАКЦИЙ в контексте существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-116">To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="dc6d1-117">Транзакции не поддерживаются для связанных таблиц.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-117">Transactions are not supported for linked tables.</span></span>

