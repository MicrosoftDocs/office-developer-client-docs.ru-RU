---
title: Метод ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713095"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="6ce3a-102">Метод ChangePassword (ADOX)</span><span class="sxs-lookup"><span data-stu-id="6ce3a-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="6ce3a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ce3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ce3a-104">Изменение пароля для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ce3a-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ce3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ce3a-105">Syntax</span></span>

<span data-ttu-id="6ce3a-106">*Пользователь*. Изменение пароля*Старый_пароль*, *Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="6ce3a-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="6ce3a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6ce3a-107">Parameters</span></span>

|<span data-ttu-id="6ce3a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="6ce3a-108">Parameter</span></span>|<span data-ttu-id="6ce3a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6ce3a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6ce3a-110">*Старый_пароль*</span><span class="sxs-lookup"><span data-stu-id="6ce3a-110">*OldPassword*</span></span> |<span data-ttu-id="6ce3a-111">**Строковое** значение, задающее существующий пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ce3a-111">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="6ce3a-112">Если у пользователя нет в настоящее время пароль, укажите пустую строку ("») для *Старый_пароль*.</span><span class="sxs-lookup"><span data-stu-id="6ce3a-112">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="6ce3a-113">*Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="6ce3a-113">*NewPassword*</span></span> |<span data-ttu-id="6ce3a-114">**Строковое** значение, задающее новый пароль.</span><span class="sxs-lookup"><span data-stu-id="6ce3a-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6ce3a-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="6ce3a-115">Remarks</span></span>

<span data-ttu-id="6ce3a-116">По соображениям безопасности старый пароль должен быть указан в дополнение к новый пароль.</span><span class="sxs-lookup"><span data-stu-id="6ce3a-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="6ce3a-117">Если поставщик поддерживает администрирования свойства доверенного лица, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="6ce3a-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

