---
title: Метод ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e7e6d88b207fecc93b9a9bafa2d6b504456a3a3e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949273"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="1655d-102">Метод ChangePassword (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1655d-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="1655d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1655d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1655d-104">Изменение пароля для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="1655d-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="1655d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1655d-105">Syntax</span></span>

<span data-ttu-id="1655d-106">*Пользователь*. Изменение пароля*Старый_пароль*, *Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="1655d-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="1655d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1655d-107">Parameters</span></span>

|<span data-ttu-id="1655d-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="1655d-108">Parameter</span></span>|<span data-ttu-id="1655d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1655d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1655d-110">*Старый_пароль*</span><span class="sxs-lookup"><span data-stu-id="1655d-110">*OldPassword*</span></span> |<span data-ttu-id="1655d-111">**Строковое** значение, задающее существующий пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="1655d-111">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="1655d-112">Если у пользователя нет в настоящее время пароль, укажите пустую строку ("») для *Старый_пароль*.</span><span class="sxs-lookup"><span data-stu-id="1655d-112">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="1655d-113">*Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="1655d-113">*NewPassword*</span></span> |<span data-ttu-id="1655d-114">**Строковое** значение, задающее новый пароль.</span><span class="sxs-lookup"><span data-stu-id="1655d-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1655d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1655d-115">Remarks</span></span>

<span data-ttu-id="1655d-116">По соображениям безопасности старый пароль должен быть указан в дополнение к новый пароль.</span><span class="sxs-lookup"><span data-stu-id="1655d-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="1655d-117">Если поставщик поддерживает администрирования свойства доверенного лица, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="1655d-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

