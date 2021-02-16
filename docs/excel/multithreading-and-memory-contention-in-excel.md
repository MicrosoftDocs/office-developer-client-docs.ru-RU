---
title: Многопрочитание и содержимое памяти в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- многопоточная протекция в Excel, скакунация памяти в Excel,функции [Excel 2007], потокобезопасные, потокобезопасные функции [Excel 2007],поток-локальная память [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301640"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Многопрочитание и содержимое памяти в Excel

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Версии Microsoft Excel более ранних версий, чем Excel 2007, используют один поток для всех вычислений листа. Однако, начиная с Excel 2007, Excel можно настроить на использование от 1 до 1024 потоков для вычисления листа. На многоядерном или многоядерном компьютере число потоков по умолчанию равно числу процессоров или ядер. Таким образом, потокобезопасные ячейки или ячейки, содержащие только потокобезопасные функции, могут быть выделены в одновредные потоки с учетом обычной логики пересчета, которая необходима для вычисления после их предыдущих предыдущих.
  
## <a name="thread-safe-functions"></a>Thread-Safe функций

Большинство встроенных функций листа, начиная с Excel 2007, потокобезопасны. Вы также можете записывать и регистрировать функции XLL как потокобезопасные. Excel использует один поток (его основной поток) для вызова всех команд, потокобезопасных функций, функций **xlAuto** (кроме [xlAutoFree](xlautofree-xlautofree12.md) и **xlAutoFree12),** а также функций COM и Visual Basic для приложений (VBA).
  
Если функция XLL возвращает **XLOPER** или **XLOPER12** с набором **xlbitDLLFree,** Excel использует тот же поток, в котором вызов функции был выполнен для вызова **xlAutoFree** или **xlAutoFree12**. Вызов **xlAutoFree** или **xlAutoFree12** происходит перед следующим вызовом функции в этом потоке. 
  
Для разработчиков XLL существуют преимущества создания потокобезопасной функции:
  
- Они позволяют Excel использовать многоядерный или многоядерный компьютер.
    
- Они открывают возможность использования удаленных серверов гораздо эффективнее, чем при использовании одного потока.
    
Предположим, что у вас есть компьютер с одним процессором, настроенный на использование, например, *потоков N.* Предположим, что выполняется таблица, которая выполняет большое количество вызовов функции XLL, которая, в свою очередь, отправляет запрос данных или вычисление для выполнения на удаленный сервер или кластер серверов. В зависимости от топологии дерева зависимостей Excel может вызывать функцию N раз почти одновременно. Если сервер или серверы достаточно быстрые или параллельные, время пересчета электронной таблицы можно сократить до 1/N. 
  
Основная проблема при написании потокобезопасных функций — правильная обработка контента для ресурсов. Как правило, это означает, что память разбита на две проблемы:
  
- Как создать память, которая будет использоваться только этим потоком.
    
- Как обеспечить безопасный доступ к общей памяти несколькими потоками.
    
Первое, что следует знать, — это то, какая память в XLL доступна всем потокам, а какая доступна только исполняемого потока.
  
 **Доступно для всех потоков**
  
- Переменные, структуры и экземпляры классов, объявленные вне тела функции.
    
- Статические переменные, объявленные в теле функции.
    
В этих двух случаях память откладывается в блоке памяти DLL, созданном для этого экземпляра DLL. Если другой экземпляр приложения загружает DLL, он получает собственную копию этой памяти, чтобы не было собружения этих ресурсов из-за пределов этого экземпляра DLL.
  
 **Доступно только для текущего потока**
  
- Автоматические переменные в коде функции (включая аргументы функции).
    
В этом случае память выделена в стеке для каждого экземпляра вызова функции.
  
> [!NOTE]
> Область динамически выделяемой памяти зависит от области указателя, на который он указывает: если указатель доступен всем потокам, память также является памятью. Если указатель является автоматической переменной в функции, выделенная память фактически является частной для этого потока. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Память, доступная только одному потоку: Thread-Local памяти

Учитывая, что статические переменные в теле функции доступны всем потокам, функции, которые их используют, явно не потокобезопасны. Один экземпляр функции в одном потоке может изменять значение, в то время как другой экземпляр в другом потоке предполагает, что это что-то совершенно другое. 
  
Существует две причины объявления статических переменных в функции:
  
1. Статические данные сохраняются при одном вызове к следующему.
    
2. Функция может безопасно вернуть указатель на статические данные.
    
В случае первой причины может потребоваться получить данные, которые сохраняются и имеют значение для всех вызовов функции: возможно, простой счетчик, который при каждом вызове функции вызывается в любом потоке, или структура, которая собирает данные об использовании и производительности при каждом вызове. Вопрос заключается в том, как защитить общие данные или структуру данных. Для этого лучше всего использовать критический раздел, как поясняется в следующем разделе.
  
Если данные предназначены только для использования этим потоком, что может быть причиной 1 и всегда является причиной 2, вопрос заключается в том, как создать память, которая сохраняется, но доступна только из этого потока. Одним из решений является использование API локального хранилища потоков (TLS).
  
Например, рассмотрим функцию, которая возвращает указатель на **XLOPER.**
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Эта функция не потокобезопасна, так как один поток может вернуть **статический XLOPER12,** а другой переописывать его. Вероятность этого по-прежнему возрастает, если **XLOPER12** необходимо передать **в xlAutoFree12.** Одним из решений является выделение **XLOPER12,** возврат на него указателя и реализация **xlAutoFree12,** чтобы освободить память **XLOPER12.** Этот подход используется во многих примерах функций, показанных в функции управления [памятью в Excel.](memory-management-in-excel.md)
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Этот подход проще реализовать, чем подход, описанный в следующем разделе, который опирается на API TLS, но имеет некоторые недостатки. Сначала Excel должен вызывать **xlAutoFree** /  **xlAutoFree12** независимо от типа **возвращенного** /  **XLOPER XLOPER12.** Во-вторых, существует проблема при возвращении  /  **XLOPER XLOPER12,** возвращаемого значением вызова функции обратного вызова API C. **XLOPER** XLOPER12 может указать на память, которая должна быть освобождена Excel, но /   **XLOPER12** /  **XLOPER12** должен быть освобожден таким же образом, как он был выделен. Если такой **XLOPER** XLOPER12 используется в качестве возвращаемого значения функции таблицы XLL, то нет простого способа сообщить /   **xlAutoFree** /  **xlAutoFree12** о необходимости освободить оба указателя соответствующим образом. (Установка **xlbitXLFree** и **xlbitDLLFree** не решает проблему, так как обработка **XLOPER/XLOPER12s** в Excel с обоими наборами не запределена и может измениться с версии на версию.) Чтобы обойти эту проблему, XLL может создавать глубокие копии всех **XLOPER/XLOPER12,** выделенных Excel, которые возвращаются на рабочий таблицу. 
  
Решение, которое позволяет избежать этих ограничений, заключается в заполнении и возвращении потока локального **XLOPER/XLOPER12**, подход, который требует, **чтобы xlAutoFree/xlAutoFree12** не освободить **сам указатель XLOPER/XLOPER12.** 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

Следующий вопрос заключается в том, как настроить и извлечь локализованную память потока, другими словами, как реализовать функцию get_thread_local_xloper12 **в** предыдущем примере. Для этого используется API локального хранилища потоков (TLS). Первым шагом является получение индекса TLS с помощью **TlsAlloc,** который в конечном итоге должен быть выпущен с помощью **TlsFree.** Оба этих решения лучше всего выполнить из **DllMain.**
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

После получения индекса необходимо выделить блок памяти для каждого потока. В [документации по](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) разработке для Windows рекомендуется делать это каждый раз при вызове функции вызова **DllMain** с событием **DLL_THREAD_ATTACH** и освободить память на каждом DLL_THREAD_DETACH **.** Тем не менее, если следовать этим рекомендациям, DLL будет делать ненужную работу для потоков, не используемых для пересчета. 
  
Вместо этого лучше использовать стратегию выделения при первом использовании. Во-первых, необходимо определить структуру, которую нужно выделить для каждого потока. В предыдущих примерах, возвращая **XLOPERs** или **XLOPER12,** можно создать любую структуру, которая удовлетворяет вашим потребностям.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Следующая функция получает указатель на локальный экземпляр потока или выделяет его, если это первый вызов.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Теперь вы можете увидеть, как получается локализованная память **потока XLOPER/XLOPER12:** сначала вы получаете указатель на экземпляр **потока TLS_data,** а затем возвращаете указатель на **XLOPER/XLOPER12,** содержащийся в нем, следующим образом. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Функции **mtr_safe_example_1** **и mtr_safe_example_2** могут быть зарегистрированы как потокобезопасные функции листа при запуске Excel. Однако нельзя смешивать два подхода в одной XLL. XLL может экспортировать только одну реализацию **xlAutoFree** и **xlAutoFree12,** и для каждой стратегии памяти требуется другой подход. При **mtr_safe_example_1** необходимо освободить указатель, переданный в **xlAutoFree/xlAutoFree12,** вместе с любыми данными, на которые он указывает. При **mtr_safe_example_2** необходимо освободить только данные с наконечнием.
  
Windows также предоставляет функцию **GetCurrentThreadId,** которая возвращает уникальный системный ИД текущего потока. Это предоставляет разработчику еще один способ сделать поток кода безопасным или сделать его поток поведения конкретным.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Память, доступная только для более чем одного потока: критические разделы

Необходимо защитить память чтения и записи, доступ к которую может получить несколько потоков с помощью критически важных разделов. Для каждого блока памяти, который требуется защитить, необходим именованый критический раздел. Вы можете инициализировать их во время вызова функции **xlAutoOpen** и освободить их и установить для них null во время вызова функции **xlAutoClose.** Затем необходимо содержать каждый доступ к защищенного блока в паре вызовов **EnterCriticalSection** и **LeaveCriticalSection.** В любой момент в критический раздел может быть разрешен только один поток. Вот пример инициализации, неинициализации и использования раздела с инициализацией **g_csSharedTable.**
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Другой, возможно, более безопасный способ защиты блока памяти —  создать класс, содержащий собственные CRITICAL_SECTION, а его использованием займется конструктор, деструктор и методы доступа. Этот подход имеет дополнительные преимущества защиты объектов, которые могут быть инициализированы до запуска **xlAutoOpen** или выдержать после того, как будет вызван **xlAutoClose,** но следует тщательно создавать слишком много критических разделов и дополнительных затрат операционной системы, которые это создаст. 
  
Если у вас есть код, которому требуется доступ к более чем одному блоку защищенной памяти одновременно, необходимо очень тщательно продумайте порядок, в котором ввели и выходят критически важные разделы. Например, следующие две функции могут создать блокировку.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Если первая функция в одном  потоке g_csSharedTableA, а вторая в другом потоке **g_csSharedTableB,** оба потока зависают. Правильный подход заключается в том, чтобы ввести согласованный порядок и выйти в обратном порядке, как поется в примере.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

По возможности лучше изолировать доступ к отдельным блокам с точки зрения совместной работы потоков, как показано ниже.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Если для общего ресурса существует большое количество запросов на доступ, таких как частые запросы на кратковременный доступ, следует рассмотреть возможность вращения критически важного раздела. Это метод, который делает ожидание ресурса менее ресурсоемким. Для этого можно использовать **initializeCriticalSectionAndSpinCount** при инициализации раздела или **SetCriticalSectionSpinCount** после инициализации, чтобы установить количество циклов потока перед ожиданием, пока ресурсы станут доступными. Операция ожидания является дорогостоящей, поэтому при закреплении этого можно избежать, если ресурс тем временем будет освобожден. В одной процессорной системе счетчик вращения фактически игнорируется, но вы все равно можете указать его, не нанося вреда. Диспетчер кучи памяти использует счетчик вращения 4000. Дополнительные сведения об использовании критически важных разделов см. в документации windows SDK. 
  
## <a name="see-also"></a>См. также



[Управление памятью в Excel](memory-management-in-excel.md)
  
[Многопоточный пересчет в Excel](multithreaded-recalculation-in-excel.md)
  
[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

