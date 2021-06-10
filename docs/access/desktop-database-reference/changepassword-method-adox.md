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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296530"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="615cc-102">Метод ChangePassword (ADOX)</span><span class="sxs-lookup"><span data-stu-id="615cc-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="615cc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="615cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="615cc-104">Изменяет пароль для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="615cc-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="615cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="615cc-105">Syntax</span></span>

<span data-ttu-id="615cc-106">*Пользователь*. *OldPassword ChangePassword*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="615cc-106">*User*.ChangePassword *OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="615cc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="615cc-107">Parameters</span></span>

|<span data-ttu-id="615cc-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="615cc-108">Parameter</span></span>|<span data-ttu-id="615cc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="615cc-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="615cc-110">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="615cc-110">*OldPassword*</span></span> |<span data-ttu-id="615cc-111">Значение **String,** которое указывает существующий пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="615cc-111">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="615cc-112">Если у пользователя в настоящее время нет пароля, используйте пустую строку ("") для *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="615cc-112">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="615cc-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="615cc-113">*NewPassword*</span></span> |<span data-ttu-id="615cc-114">Значение **String,** которое указывает новый пароль.</span><span class="sxs-lookup"><span data-stu-id="615cc-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="615cc-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="615cc-115">Remarks</span></span>

<span data-ttu-id="615cc-116">В целях безопасности старый пароль должен быть указан в дополнение к новому.</span><span class="sxs-lookup"><span data-stu-id="615cc-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="615cc-117">Ошибка произойдет, если поставщик не поддерживает администрирование свойств доверяемого.</span><span class="sxs-lookup"><span data-stu-id="615cc-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

