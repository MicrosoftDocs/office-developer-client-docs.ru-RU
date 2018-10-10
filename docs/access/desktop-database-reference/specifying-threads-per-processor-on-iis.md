---
title: Specifying Threads Per Processor on IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480355"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="ad3b6-102">Specifying Threads Per Processor on IIS</span><span class="sxs-lookup"><span data-stu-id="ad3b6-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="ad3b6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad3b6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad3b6-104">При использовании служб удаленных рабочих СТОЛОВ с помощью Internet Information Services 4.0 или более поздней версии, количество потоков, созданных на процессор можно управлять с помощью управления реестра на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server.</span></span> <span data-ttu-id="ad3b6-105">Количество потоков процессора может повлиять на производительность в случае большой сетевой трафик, или в ситуациях низкой трафика с помощью запроса большого размера.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="ad3b6-106">Пользователю следует проверить для достижения наилучших результатов.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-106">The user should experiment for best results.</span></span>

<span data-ttu-id="ad3b6-107">Метод, используемый для определения и измените значение по умолчанию для этого параметра зависит от конфигурации сервера IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="ad3b6-108">С MDAC 2.1.2.4202.3 (Джорджия) или более поздней версии на сервере IIS использует служб удаленных рабочих СТОЛОВ же службы компонентов (или транзакций Microsoft Services, если вы используете Windows NT) пул потоков как ASP сценариев использования.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-108">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use.</span></span> <span data-ttu-id="ad3b6-109">Значение по умолчанию для числа потоков на процессор — 10.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-109">The default value for the number of threads per processor is 10.</span></span> <span data-ttu-id="ad3b6-110">Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел реестра сервера:</span><span class="sxs-lookup"><span data-stu-id="ad3b6-110">To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="ad3b6-111">где *MaxPoolThreads* — REG\_значение DWORD.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="ad3b6-112">*MaxPoolThreads* не отображается в реестре, если он добавляется в частности.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="ad3b6-113">Диапазон допустимых значений от 5 рекомендуемый максимум 20.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="ad3b6-114">Если значение, указанное в ключе реестра больше, чем значение параметра *PoolThreadLimit* (находится в разделе тот же путь), используется значение *PoolThreadLimit* .</span><span class="sxs-lookup"><span data-stu-id="ad3b6-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="ad3b6-115">Кроме того Если MDAC 2.1 2.1.1.3711.11 (Джорджия) или более ранних версий установлен на сервере служб IIS, значение по умолчанию для числа потоков процессора, 6.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-115">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6.</span></span> <span data-ttu-id="ad3b6-116">Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел реестра на сервере IIS:</span><span class="sxs-lookup"><span data-stu-id="ad3b6-116">To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="ad3b6-117">где *ADCThreads* — REG\_значение DWORD.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="ad3b6-118">*ADCThreads* не отображается в реестре, если он добавляется в частности.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="ad3b6-119">Диапазон допустимые значения — от 1 до 50.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="ad3b6-120">Если значение, указанное в ключе реестра больше 50, максимальное значение — используемых (50).</span><span class="sxs-lookup"><span data-stu-id="ad3b6-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

