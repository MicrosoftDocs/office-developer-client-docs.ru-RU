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
ms.openlocfilehash: f48b1ab98f6f0f729fdb32b4ff20be09c5d942bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886391"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="582f4-102">Оператор ТРАНЗАКЦИЙ (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="582f4-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="582f4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="582f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="582f4-104">Используется для начинать и завершать явные операции.</span><span class="sxs-lookup"><span data-stu-id="582f4-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="582f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="582f4-105">Syntax</span></span>

<span data-ttu-id="582f4-106">**Начало новой операции**:</span><span class="sxs-lookup"><span data-stu-id="582f4-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="582f4-107">НАЧАТЬ ТРАНЗАКЦИЮ</span><span class="sxs-lookup"><span data-stu-id="582f4-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="582f4-108">**Conclude транзакций с внесением всех рабочих выполнена во время операции**:</span><span class="sxs-lookup"><span data-stu-id="582f4-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="582f4-109">ФИКСАЦИЯ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="582f4-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="582f4-110">**Conclude транзакций с помощью отката все действия выполняются во время операции**:</span><span class="sxs-lookup"><span data-stu-id="582f4-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="582f4-111">ОТКАТ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="582f4-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="582f4-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="582f4-112">Remarks</span></span>

<span data-ttu-id="582f4-113">Не удалось автоматически запустить транзакции.</span><span class="sxs-lookup"><span data-stu-id="582f4-113">Transactions are not started automatically.</span></span> <span data-ttu-id="582f4-114">Чтобы запустить операцию, необходимо выполнить явно использовать команду НАЧАТЬ ТРАНЗАКЦИЙ.</span><span class="sxs-lookup"><span data-stu-id="582f4-114">To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="582f4-115">Операции могут быть вложенными до пяти уровней вложенности.</span><span class="sxs-lookup"><span data-stu-id="582f4-115">Transactions can be nested up to five levels deep.</span></span> <span data-ttu-id="582f4-116">Чтобы начать вложенных транзакций, используйте приступить к ТРАНЗАКЦИЙ в контексте существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="582f4-116">To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="582f4-117">Транзакции не поддерживаются для связанных таблиц.</span><span class="sxs-lookup"><span data-stu-id="582f4-117">Transactions are not supported for linked tables.</span></span>

