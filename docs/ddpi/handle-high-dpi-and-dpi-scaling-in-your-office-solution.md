---
title: Обработка высокого разрешения и масштабирования в решении для Office
description: Для поддержки мониторов с высоким разрешением обновите свое решение для Office, например настраиваемые области задач и элементы ActiveX.
ms.date: 03/09/2019
localization_priority: Normal
ms.openlocfilehash: 0425e5e9dd0f060a6336888cfe6c236b39732080
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980469"
---
# <a name="handle-high-dpi-and-dpi-scaling-in-your-office-solution"></a>Обработка высокого разрешения и масштабирования в решении для Office

Многие конфигурации компьютеров и мониторов теперь поддерживают высокие разрешения (количество точек на дюйм) и обеспечивают возможность подключения нескольких мониторов c разными размерами и плотностью пикселей. Для этого приложениям требуется выполнять настройку, если пользователь перемещает их на монитор с другим разрешением или изменяет масштаб. Приложения, не поддерживающие масштабирование, могут выглядеть нормально на мониторах c низким разрешением, но будут растянутыми и размытыми при отображении на мониторах с высоким разрешением. 

Приложения Office 2016, такие как Word и Excel, были обновлены, чтобы реагировать на изменения коэффициента масштаба. Однако решение для Office также должно реагировать на изменения, чтобы правильно отображаться. В этой статье описано, как Office поддерживает динамическое разрешение и какие действия можно предпринять, чтобы обеспечить оптимальный интерфейс просмотра для решения по расширению Office при использовании масштабирования. 

## <a name="dpi-scaling-symptoms-in-your-solution"></a>Проблемы масштабирования в решении

Windows применяет масштабирование, если приложение перемещается между мониторами с разным разрешением. Это происходит в таких случаях, как перетаскивание приложения на другой монитор или подключение ноутбука. Если масштабирование негативно влияет на решение для Office, появится одна или несколько из указанных ниже проблем.

- Окно отображается в неправильном месте или с неправильным размером.
- Элементы, например кнопки и подписи, отображаются в неправильном месте окна решения.
- Шрифты и изображения отображаются слишком маленькими, слишком большими или в неправильном месте.

Ниже указаны типы решений для Office, на которые может влиять масштабирование.

- Надстройки VSTO
- Настраиваемые области задач
- Надстройки COM
- Элементы ActiveX
- Расширения ленты
- OLE-серверы
- Веб-надстройки Office

## <a name="windows-dpi-awareness-modes"></a>Режимы поддержки определения DPI Windows

В этой статье используются режимы поддержки определения DPI, допустимые в Windows. Каждый из режимов поддержки определения DPI допускает применение разных возможностей, как указано в таблице ниже. Это упрощенное описание режимов для объяснения способов их поддержки решениями для Office. Дополнительные сведения о режимах поддержки определения DPI см. в статье [Разработка классических приложений с высоким разрешением для Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).

|Режим  |Описание  |При изменении разрешения  |
|---------|---------|---------|
|Без поддержки определения DPI |  Приложение всегда отображается как для дисплея со значением 96 точек на дюйм. |  Приложение — растровое изображение, растянутое до нужного размера на основном и дополнительном дисплеях.    |
|Поддержка определения DPI на уровне системы |  Приложения определяют разрешение основного подключенного монитора при входе в Windows, но не могут реагировать на изменение разрешения. Для получения дополнительных сведений обратитесь к разделу [Настройка Windows для устранения размытых приложений](#configure-windows-to-fix-blurry-apps) в этой статье.  | Приложение — растровое изображение, растягиваемое при перемещении на новый дисплей с другим разрешением.    |
|Поддержка определения DPI на уровне монитора |  При изменении разрешения приложение может правильно изменить свое отображение.  |   Windows отправляет уведомления о разрешении для окон верхнего уровня в приложении, чтобы оно могло изменить отображение при изменении разрешения.     |
|На уровне монитора версия 2 |  При изменении разрешения приложение может правильно изменить свое отображение.  |   Windows отправляет уведомления о разрешении для окон верхнего и дочернего уровня, чтобы приложение могло изменить отображение при изменении разрешения. |

## <a name="how-office-supports-dpi-scaling"></a>Как Office поддерживает масштабирование

Самый важный фактор при определении способа обработки масштабирования решением для Office состоит в том, является ли ваше решение окном верхнего или дочернего уровня. На рисунке ниже показано несколько примеров решений для Office, работающих как окна верхнего или дочернего уровня, а также применяемый ими режим поддержки определения DPI в обновлении Windows за апрель 2018 г. (1803) или более позднем.

![Excel с элементом ActiveX и настраиваемой областью задач в виде дочерних окон. Отдельная надстройка VSTO или COM, запущенная как окно верхнего уровня. Office — это окно верхнего уровня.](./media/office-dpi-awareness-for-solution-types.png)

На этом рисунке:
- Окно верхнего уровня COM или VSTO использует поддержку определения DPI на уровне монитора.
- Дочернее окно элемента ActiveX использует поддержку определения DPI на уровне системы.
- Окно верхнего уровня Office использует поддержку определения DPI на уровне монитора.
- Дочернее окно настраиваемой области задач использует поддержку определения DPI на уровне системы.

## <a name="managing-thread-dpi-context"></a>Управление контекстом DPI потока

При запуске ведущего приложения Office его основной поток выполняется в контексте поддержки определения DPI на уровне монитора. Если код решения создает потоки или получает вызовы от Office, требуется управлять контекстом DPI потока.

### <a name="creating-new-threads-with-the-correct-dpi-context"></a>Создание новых потоков с правильным контекстом DPI

Если ваше решение создает дополнительные потоки, Office принудительно переводит эти потоки в контекст поддержки определения DPI на уровне монитора. Если в вашем коде предполагается другой контекст, необходимо использовать функцию [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) для установки нужной поддержки определения DPI потока. 

### <a name="build-a-context-block-for-incoming-thread-calls"></a>Создание контекстного блока для входящих вызовов потока

![Схема, показывающая контекстный блок в приложении Office, который переключает поток на контекст поддержки определения на уровне системы для вызовов к окну верхнего уровня.](./media/thread-dpi-awareness-context-block.png)

Ваше решение взаимодействует с ведущим приложением Office, поэтому в решение будут поступать входящие вызовы от Office, например обратные вызовы событий. Когда Office вызывает решение, используется контекстный блок, принудительно устанавливающий в качестве контекста потока поддержку определения DPI на уровне системы. Необходимо изменить контекст потока в соответствии с поддержкой определения DPI вашего окна. Можно реализовать похожий контекстный блок, чтобы переключать контекст потока для входящих вызовов. Используйте функцию [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext), чтобы изменить контекст в соответствии с контекстом вашего окна. 

> [!NOTE]
> Ваш контекстный блок должен восстановить исходный контекст DPI потока перед вызовом других компонентов за пределами кода решения.

#### <a name="managed-code-context-block"></a>Контекстный блок управляемого кода

В приведенном ниже примере кода показано, как создать собственный контекстный блок.

```csharp
public struct DPI_AWARENESS_CONTEXT
        {
            private IntPtr value;

            private DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                this.value = value;
            }

            public static implicit operator DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                return new DPI_AWARENESS_CONTEXT(value);
            }

            public static implicit operator IntPtr(DPI_AWARENESS_CONTEXT context)
            {
                return context.value;
            }

            public static bool operator ==(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return AreDpiAwarenessContextsEqual(context1, context2);
            }

            public static bool operator !=(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return !AreDpiAwarenessContextsEqual(context1, context2);
            }

            public override bool Equals(object obj)
            {
                return base.Equals(obj);
            }

            public override int GetHashCode()
            {
                return base.GetHashCode();
            }
        }

        private static DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_HANDLE = IntPtr.Zero;

        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_INVALID = IntPtr.Zero;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_UNAWARE = new IntPtr(-1);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_SYSTEM_AWARE = new IntPtr(-2);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE = new IntPtr(-3);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 = new IntPtr(-4);

        public static DPI_AWARENESS_CONTEXT[] DpiAwarenessContexts =
        {
            DPI_AWARENESS_CONTEXT_UNAWARE,
            DPI_AWARENESS_CONTEXT_SYSTEM_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
        };

class DPIContextBlock : IDisposable
    {
        private DPI_AWARENESS_CONTEXT resetContext;
        private bool disposed = false;

        public DPIContextBlock(DPI_AWARENESS_CONTEXT contextSwitchTo)
        {
            resetContext = SetThreadDpiAwarenessContext(contextSwitchTo);
         }

        public void Dispose()
        {
            Dispose(true);
            GC.SuppressFinalize(this);
        }

        protected virtual void Dispose(bool disposing)
        {
            if (!disposed)
            {
                if (disposing)
                {
                    SetThreadDpiAwarenessContext(resetContext);
                }
            }
            disposed = true;
        }
    }
```

#### <a name="native-code-context-block"></a>Контекстный блок машинного кода

```cpp
#include <winuser.h>
/* DpiAwarenessContextBlock can be used to simplify setting and resetting the DPI_AWARENESS_CONTEXT of
the current thread.  When the object is constructed, the DPI_AWARENESS_CONTEXT is set, and when the object is
destructed, the DPI awareness context is reverted to the previous awareness context at construct time.

This object allows us to write code such as:

// Thread state is currently DPI_AWARENESS_SYSTEM_AWARE
if (condition)
{
DpiAwarenessContextBlock perMonitorAware(DPI_AWARENESS_PER_MONITOR_AWARE);
... // Create a top-level hwnd with the current thread state, DPI_AWARENESS_PER_MONITOR_AWARE
}
// Thread state automatically returns to DPI_AWARENESS_SYSTEM_AWARE

*/
class DpiAwarenessContextBlock
{
public:
      DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept;
      ~DpiAwarenessContextBlock();

      // Copy and move are not to be used with these context objects
      DpiAwarenessContextBlock(const DpiAwarenessContextBlock&) = delete;
      DpiAwarenessContextBlock(DpiAwarenessContextBlock&&) = delete;

private:
      DPI_AWARENESS_CONTEXT m_contextReversalType;
      bool m_doContextSwitch;
};

inline DpiAwarenessContextBlock::DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept
{
      m_contextReversalType = SetThreadDpiAwarenessContext(dpiContext);
}

inline DpiAwarenessContextBlock::~DpiAwarenessContextBlock()
{
      SetThreadDpiAwarenessContext(m_contextReversalType);
}
```

<h2 id="top-level-window-management">Управление окнами верхнего уровня</h2>

При запуске приложения Office вызывается функция [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) как DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE. В этом контексте изменения разрешения отправляются в свойство HWND любого окна верхнего уровня в процессе, выполняемом с поддержкой определения DPI на уровне монитора. Окна верхнего уровня — это окно приложения Office и все дополнительные окна верхнего уровня, созданные вашим решением. При перемещении приложения Office на новый дисплей оно получает уведомление, чтобы иметь возможность динамически изменить масштаб и правильно отобразиться в разрешении нового дисплея. Решение для Office может создавать окна верхнего уровня с любым режимом поддержки определения DPI. Ваши окна верхнего уровня также могут реагировать на изменения разрешения, прослушивая сообщения Windows на изменения.

Если вы создаете окна, дочерние по отношению к родительскому окну верхнего уровня, для них можно установить любой режим поддержки определения DPI. Однако при использовании режима поддержки определения DPI на уровне монитора дочерние окна не будут получать уведомления об изменении разрешения.  Дополнительные сведения о режимах поддержки определения DPI в Windows см. в статье [Разработка классических приложений с высоким разрешением для Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).

## <a name="child-window-management"></a>Управление дочерними окнами

При работе с элементами ActiveX и настраиваемыми областями задач Office создает дочернее окно для вашего решения. Вы можете создать дополнительные дочерние окна, но нужно учитывать режим поддержки определения DPI родительского окна. Office работает в режиме поддержки определения DPI на уровне монитора. Это означает, что ни одно дочернее окно в решении не будет получать уведомления об изменении разрешения. Только режим на уровне монитора версии 2 поддерживает отправку изменений разрешения дочерним окнам (Office не поддерживает режим на уровне монитора версии 2). Однако для элементов ActiveX есть обходное решение. Дополнительные сведения см. ниже в разделе [Элементы ActiveX](#activex-controls).

> [!NOTE]
> Если дочернее окно создает окно верхнего уровня, можно использовать любой режим поддержки определения DPI для нового окна верхнего уровня. Дополнительные сведения об управлении окнами верхнего уровня см. в разделе [Управление окнами верхнего уровня](#top-level-window-management) этой статьи.

В зависимости от версии Windows 10, на которой работает Office, к дочернему окну могут применяться два разных режима поддержки определения DPI.

### <a name="office-dpi-behavior-on-windows-fall-creators-update-1709"></a>Режим DPI для Office в Windows Fall Creators Update (1709)

Так как в приложениях Office используется режим поддержки определения на уровне монитора, дочерние окна вашего решения также создаются в этом режиме. Это означает, что Windows ожидает обновления вашего решения при отображении в новом разрешении.  Так как ваше окно не может получать уведомления об изменении разрешения, пользовательский интерфейс решения может отображаться неправильно. 

![Схема, показывающая дочерние окна, запущенные в контексте поддержки определения DPI на уровне монитора в обновлении Windows Fall Creators Update (1709).](./media/office-dpi-behavior-on-windows-fall-creators-update.png)

### <a name="office-dpi-behavior-on-windows-april-2018-update-1803"></a>Режим DPI для Office в обновлении Windows за апрель 2018 г. (1803)

В обновлении Windows за апрель 2018 г. (1803) и более поздних версиях в качестве режима DPI ведущего приложения Office используется смешанный режим масштабирования для некоторых сценариев. Это позволяет окнам с поддержкой определения DPI на уровне системы использовать в качестве родительских окна Office с режимом поддержки определения DPI на уровне монитора. Это помогает улучшить совместимость при изменениях разрешения, если окна являются растянутыми растровыми изображениями. Окна по-прежнему могут отображаться размыто из-за растяжения растрового изображения.

![Схема, показывающая дочерние окна, запущенные в контексте поддержки определения DPI на уровне системы в обновлении Windows за апрель 2018 г. (1803).](./media/office-dpi-behavior-on-windows-april-2018-update.png)

При создании новых дочерних окон убедитесь, что их поддержка определения DPI соответствует родительскому окну. Можно использовать функцию [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext), чтобы получить режим поддержки определения DPI родительского окна. Дополнительные сведения о согласовании поддержки определения DPI см. в разделе "Принудительный сброс поддержки определения DPI на уровне процесса" статьи [Разработка классических приложений с высоким разрешением для Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).

> [!NOTE]
> Нельзя полагаться на поддержку определения DPI на уровне процесса, поскольку она может вернуть значение [PROCESS_SYSTEM_DPI_AWARE](https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness), даже если контекст поддержки определения DPI основного потока приложения соответствует значению [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context). Используйте функцию [GetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext), чтобы получить контекст поддержки определения DPI потока.

## <a name="office-and-windows-dpi-compatibility-settings"></a>Параметры совместимости разрешений Office и Windows

Если надстройки или решения отображаются неправильно, можно использовать параметры совместимости, которые могут помочь исправить проблему.

<h3 id="office-compatibility">Настройка Office для оптимизации обеспечения совместимости</h3>

В Office есть настройка оптимизации для обеспечения совместимости при переходе на другой масштаб на разных экранах. Режим совместимости отключает масштабирование, чтобы в качестве всех элементов Office использовалось растровое изображение, растягиваемое при перемещении на дисплей с другим масштабом. 

Режим совместимости принудительно переводит Office в режим поддержки определения DPI на уровне системы. Это приводит к растягиванию растровых изображений окон приложения и в качестве побочного эффекта может вызывать размытый внешний вид. Ваше решение для Office не может управлять этой настройкой, так как ее выбирает пользователь. Использование режима совместимости дисплея решает большинство проблем отображения. Дополнительные сведения см. в статье [Поддержка мониторов с высоким разрешением в Office](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d). 

### <a name="configure-windows-to-fix-blurry-apps"></a>Настройка Windows для исправления размытых приложений

В Windows 10 (версия 1803) и более поздних версиях есть настройка, исправляющая размытость приложения. Это еще одна настройка, которой можно воспользоваться, если решение отображается неправильно. Ваше решение для Office не может управлять этой настройкой, так как ее выбирает пользователь. Дополнительные сведения см. в статье [Исправление размытости приложений в Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).

## <a name="how-to-support-dpi-scaling-in-your-solution"></a>Поддержка масштабирования в решении

Некоторые решения могут получать уведомления об изменениях разрешения и реагировать на них. В некоторых есть обходное решение, если они не могут получать уведомления. В таблице ниже перечислены сведения для каждого типа решения.

<table>
    <thead>
        <tr>
            <th>Тип решения</th>
            <th>Тип окна</th>
            <th>Возможность реакции на масштабирование</th>
            <th>Дополнительные сведения</th>
        </tr>
    </thead>
<tbody>
    <tr>
        <td rowspan="2"><a href="#vsto-add-ins">Надстройка VSTO</a></td>
        <td>Верхний уровень и его дочерние окна</td>
        <td>Да</td>
        <td>См. <a href="#vsto-add-ins">рекомендации для надстройки VSTO</a>.</td>
    </tr>
<tr>
        <td>Дочерние для родительского окна Office</td>
        <td>Нет</td>
        <td>См. <a href="#office-compatibility">Настройка Office для оптимизации обеспечения совместимости</a>.</td>
</tr>
    <tr>
        <td rowspan="2"><a href="#custom-task-panes">Настраиваемая область задач</a></td>
        <td>Верхний уровень и его дочерние окна</td>
        <td>Да</td>
        <td>См. <a href="#top-level-window-management">рекомендации для окна верхнего уровня</a>.</td>
    </tr>
<tr>
        <td>Дочерние для родительского окна Office</td>
        <td>Нет</td>
        <td>См. <a href="#office-compatibility">Настройка Office для оптимизации обеспечения совместимости</a>.</td>
</tr>
    <tr>
        <td rowspan="2"><a href="#com-add-ins">Надстройка COM</a></td>
        <td>Верхний уровень и его дочерние окна</td>
        <td>Да</td>
        <td>См. <a href="#com-add-ins">рекомендации для надстройки COM</a>.</td>
    </tr>
<tr>
        <td>Дочерние для родительского окна Office</td>
        <td>Нет</td>
        <td>См. <a href="#office-compatibility">Настройка Office для оптимизации обеспечения совместимости</a>.</td>
</tr>
    <tr>
        <td rowspan="2"><a href="#activex-controls">Элемент ActiveX</a></td>
        <td>Верхний уровень и его дочерние окна</td>
        <td>Да</td>
        <td>См. <a href="#activex-controls">рекомендации для элемента ActiveX</a>.</td>
    </tr>
    <tr>
        <td>Дочерние для родительского окна Office</td>
        <td>Да</td>
    </tr>
    <tr>
        <td><a href="#web-add-ins">Веб-надстройка</a></td>
        <td>Н/Д</td>
        <td>Да</td>
        <td>См. <a href="#web-add-ins">рекомендации для веб-надстройки Office</a>.</td>
    </tr>
    <tr>
        <td><a href="#ribbon-extensibility">Расширение ленты</a></td>
        <td>Недоступно</td>
        <td>Недоступно</td>
        <td>См. <a href="#ribbon-extensibility">рекомендации для расширения ленты</a>.</td>
    </tr>
    <tr>
        <td><a href="#ole">OLE-сервер или клиент</a></td>
        <td>Недоступно</td>
        <td>Недоступно</td>
        <td>См. <a href="#ole">рекомендации для OLE-сервера или клиента</a>.</td>
    </tr>
</tbody>
</table>

<h3 id="vsto-add-ins">Надстройка VSTO</h3>

Если надстройка VSTO создает окна, дочерние по отношению к любому родительскому окну Office, убедитесь, что их поддержка определения DPI соответствует родительскому окну. Можно использовать функцию [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext), чтобы получить режим поддержки определения DPI родительского окна. Дочерние окна не будут получать уведомлений об изменении разрешения. Если ваше решение отображается неправильно, пользователям нужно будет перевести Office в режим совместимости.

Для любого окна верхнего уровня, создаваемого надстройкой VSTO, можно установить любой режим поддержки определения DPI. В приведенном ниже примере кода показано, как настроить нужную поддержку определения DPI и как реагировать на изменения разрешения. Вам также потребуется настроить app.config, как описано в статье [Поддержка высокого разрешения в Windows Forms](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms). 

```csharp
using System;
using System.Diagnostics;
using System.Drawing;
using System.Runtime.InteropServices;
using System.Windows.Forms;

namespace SharedModule
{
    // DpiAwareWindowsForm
    // For any top level winform you create, derive from the DpiWindowsForm class
    // if you are creating Windows Forms with the Dpi Awareness Context set to 
    // DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE or DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
    //
    // For example, if you Window form class is defined as:
    //    public partial class TopLevelWinForm : Form
    //
    // update to:
    //    public partial class TopLevelWinForm : DpiAwareWindowsForm
    //
    // When showing the form, call SetThreadDpiAwarenessContext() or use a context block to
    // to set the desired Dpi Awareness Context.
    //
    // For example, here is code to show a Windows Form using a context block as Per Monitor Aware v2.
    //
    //    DPIContextBlock context = new DPIContextBlock(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2);
    //    TopLevelWinForm frm = new TopLevelWinForm();
    //    frm.Show();
    //
    public partial class DpiAwareWindowsForm : Form
    {
        private SizeF m_newDpi = SizeF.Empty;
        private SizeF m_oldDpi = SizeF.Empty;

        public DpiAwareWindowsForm()
        {
            this.HandleCreated += new EventHandler((sender, args) =>
            {
                m_oldDpi = m_newDpi = DPIHelper.GetDpiForWindowSizeF(this.Handle);
            });
        }

        public void OnDpiChangedEvent(RECT newRect)
        {
            this.SuspendLayout();

            // Resize form
            this.Width = newRect.Width;
            this.Height = newRect.Height;

            // Resize controls and set font sizes
            ScaleAllChildControls(this.Controls, m_oldDpi.Width, m_newDpi.Width);
            this.ResumeLayout(true);
        }

        // Additional changes may be needed for controls that set Anchor or Dock properties 
        private void ScaleAllChildControls(Control.ControlCollection controls, float oldDpi, float newDpi)
        {
            float scaleFactorChange = newDpi / oldDpi;

            foreach (Control control in controls)
            {
                control.Top = (int)(control.Top * scaleFactorChange);
                control.Left = (int)(control.Left * scaleFactorChange);
                control.Width = (int)(control.Width * scaleFactorChange);
                control.Height = (int)(control.Height * scaleFactorChange);
                control.Font = ScaleFont(control.Font, oldDpi, newDpi);
            }
        }

        private Font ScaleFont(Font font, float oldDpi, float newDpi)
        {
            float fontSizePx = 0.0f;
            float fontSizePt = 0.0f;

            fontSizePx = font.SizeInPoints / 72 * oldDpi;
            fontSizePt = fontSizePx * (newDpi / oldDpi) * 72 / oldDpi;

            return new Font(font.Name, fontSizePt, font.Style, GraphicsUnit.Point);
        }

        protected override void WndProc(ref Message m)
        {
            switch ((DPIHelper.WinMessages)m.Msg)
            {
                case DPIHelper.WinMessages.WM_DPICHANGED:
                    // Marshal the value in the lParam into a Rect.
                    RECT newDisplayRect = (RECT)Marshal.PtrToStructure(m.LParam, typeof(RECT));

                    // Remember current DPI and calculate current from WParam.
                    // Both X and Y are the same on Windows for Dpi.
                    m_oldDpi = m_newDpi;

                    m_newDpi.Width = (float)(m.WParam.ToInt32() >> 16);
                    m_newDpi.Height = (float)(m.WParam.ToInt32() & 0x0000FFFF);

                    // DPI should be the same for both width and height on Windows devices.
                    Debug.Assert(m_newDpi.Height == m_newDpi.Width);

                    if (m_oldDpi.Width != m_newDpi.Width)
                    {
                        OnDpiChangedEvent(newDisplayRect);
                    }
                    base.DefWndProc(ref m);
                    break;
                default:
                    base.WndProc(ref m);
                    break;
            }
        }
    }
}
```

<h3 id="custom-task-panes">Настраиваемые области задач</h3>

Настраиваемая область задач создается приложением Office в виде дочернего окна. При использовании обновления Windows Fall Creators Update (1709) настраиваемая область задач запускается с использованием такого же режима поддержки определения DPI, как в Office. При использовании обновления Windows за апрель 2018 г. (1803) и более поздней версии настраиваемая область задач запускается с использованием режима поддержки определения DPI на уровне системы. 

Так как настраиваемые области являются дочерними окнами, они не могут получать уведомления о разрешении. Если они отображаются неправильно, пользователю потребуется использовать [Режим совместимости разрешений в Office](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).
Если настраиваемая область задач создает окна верхнего уровня, эти окна могут запускаться в любом режиме поддержки определения DPI и получать уведомления об изменении разрешения. Дополнительные сведения см. в разделе [Управление окнами верхнего уровня](#top-level-window-management) этой статьи.

<h3 id="com-add-ins">Надстройки COM</h3>

Надстройки COM, создающие окна верхнего уровня могут получать уведомления об разрешении. Необходимо создать [контекстный блок](#build-a-context-block-for-incoming-thread-calls) и установить для потока поддержку определения DPI, необходимую для окна, а затем создать окно. Существует много нюансов для правильной обработки уведомлений о разрешении, поэтому обязательно ознакомьтесь с дополнительными сведениями в статье [Разработка классических приложений с высоким разрешением для Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).

Сообщение [WM_DPICHANGED](https://docs.microsoft.com/windows/desktop/hidpi/wm-dpichanged) отправляется при изменении разрешения для окна.  В неуправляемом коде это сообщение обрабатывается с помощью [процедуры окна](https://docs.microsoft.com/windows/desktop/winmsg/using-window-procedures) для свойства HWND.  Пример кода обработчика изменения разрешения можно найти в статье WM_DPICHANGED. 

Надстройки COM, отображающие окна, дочерние по отношению к родительскому окну в Office, не могут получать уведомления о разрешении. Если они отображаются неправильно, пользователю потребуется использовать [Режим совместимости разрешений в Office](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).

<h3 id="activex-controls">Элементы ActiveX</h3>

Способ поддержки масштабирования в элементах ActiveX зависит от того, есть ли у элемента окна или нет.

#### <a name="windowed-activex-controls"></a>Элементы ActiveX с окнами

Элементы ActiveX с окнами получают сообщение, WM_SIZE каждый раз, когда изменяется размер элемента.  При возникновении этого события код обработчика события может вызвать функцию [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) с помощью свойства HWND элемента управления, чтобы получить значение разрешения, рассчитать разницу коэффициентов масштаба и выполнить соответствующую настройку. 

В приведенном ниже примере включается элемент ActiveX на основе MFC, чтобы ответить на событие **OnSize**. 

```cpp
void ChangeWindowFontDPI(HWND hWnd, UINT dpi) 
{ 
LOGFONT fontInfo1 = { 0 }; 
// Calculate the font height based on the DPI. 
fontInfo1.lfHeight = -MulDiv(DESIRED_HEIGHT, dpi, 72); 
fontInfo1.lfQuality = CLEARTYPE_QUALITY; 
wcscpy_s(fontInfo1.lfFaceName, DESIRED_FONT_NAME); 
 
::SendMessage(hWnd, WM_SETFONT, (WPARAM)::CreateFontIndirectW(&fontInfo1), TRUE); 
} 
 
BOOL CALLBACK CMainDialog::EnumChildProc(HWND hWnd, LPARAM lParam) 
{ 
CMainDialog* _this = (CMainDialog*) lParam; 
if (_this != nullptr) 
{ 
// Calculate the scale factor difference between the old and new DPI changes. 
double scale = (((double) _this->m_newDPI) /  
   (((double) _this->m_currentDPI) / 100.0)) / 100; 
 
RECT rect = {}; 
::GetWindowRect(hWnd, &rect); 
 
POINT pt = { rect.left, rect.top }; 
::ScreenToClient(::GetParent(hWnd), &pt); 
 
// Adjust the window based on the scale changes. 
::MoveWindow(hWnd, 
pt.x * scale, 
pt.y * scale, 
(rect.right - rect.left) * scale, 
(rect.bottom - rect.top) * scale, 
TRUE); 
 
ChangeWindowFontDPI(hWnd, _this->m_newDPI); 
return TRUE; 
} 
return FALSE; 
} 
 
void CMainDialog::OnSize(UINT nType, int cx, int cy) 
{ 
CDialog::OnSize(nType, cx, cy); 
 
// Get the new DPI and enumerate the child windows that will use that value. 
m_currentDPI = ::GetDpiForWindow(this->GetSafeHwnd()); 
::EnumChildWindows(this->GetSafeHwnd(), EnumChildProc, (LPARAM)this); 
} 
```

#### <a name="windowless-activex-controls"></a>Элементы ActiveX без окон

Для элементов ActiveX без окон не гарантировано наличие свойства HWND.  Когда элемент ActiveX добавляется на холст документа, он переводится в режим конструктора.  В приложениях Office размещающий контейнер возвращает 0 при вызове hDC -> GetWindow() в событии ::OnDraw, если элемент управления находится в режиме конструктора.  В этом случае нельзя получить надежное значение разрешения. 

Однако если элемент управления находится в режиме выполнения, Office вернет свойство HWND, где должен отображаться элемент управления.  В этом случае разработчик элемента управления может вызвать функцию [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) и получить текущее разрешение, а также шрифты масштабирования, элементы управления и т. д. 

<h3 id="ribbon-extensibility">Возможности расширения настраиваемой ленты</h3>

Любые обратные вызовы из Office для элементов управления настраиваемой ленты будут выполняться в потоке с поддержкой определения DPI на уровне системы.  Если решение ожидает другой режим поддержки определения DPI потока, следует внедрить контекстный блок, чтобы установить нужный режим поддержки определения для потока. Дополнительные сведения см. в разделе [Создание контекстного блока](#build-a-context-block-for-incoming-thread-calls).

<h3 id="ole">OLE-серверы и клиенты</h3>

Если OLE-сервер размещен в контейнере OLE клиента, в настоящее время нельзя предоставить сведения о текущем или поддерживаемом разрешении. Это может привести к проблемам, так как некоторые сочетания родительского и дочернего окон с разными режимами не поддерживаются в текущей архитектуре Windows. Если Word или Excel обнаруживают наличие нескольких мониторов с разными масштабами, они не будут поддерживать встроенную активацию. Активация OLE-сервера выполняется "не на месте". Если возникают проблемы при взаимодействии с OLE-сервером, пользователю потребуется использовать [Режим совместимости разрешений в Office](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).

<h3 id="web-add-ins">Веб-надстройки Office</h3>

Веб-надстройки Office созданные с помощью API JavaScript для Office, запускаются внутри элемента управления браузера. Обрабатывать масштабирование можно с помощью тех же методов, которые используются при разработке любого веб-приложения. Существует много сетевых ресурсов, помогающих разработать веб-страницу для экранов с высоким разрешением.

## <a name="verify-that-your-solution-supports-dpi-scaling"></a>Проверка того, что решение поддерживает масштабирование

После обновления приложения для поддержки масштабирования необходимо проверить изменения в среде с разными разрешениями. Убедитесь, что ваш код пользовательского интерфейса правильно реагирует на изменения разрешения, когда окно решения перемещается между дисплеями с разными значениями разрешений. Дополнительные сведения о методах проверки масштабирования см. в статье [Разработка классических приложений с высоким разрешением для Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).

Вы также могут пригодиться эти дополнительные методы:

- При использовании ноутбука можно установить основной монитор на внешнем мониторе, затем отсоединить ноутбук. Это приведет к принудительному переключению основного монитора на дисплей ноутбука.
- Используйте [средство WinSpy ++](https://github.com/BissetJ/winspy/releases) с открытым кодом для помощи в отладке. Его можно использовать для просмотра настройки поддержки определения DPI любого окна.
- Также можно использовать удаленный рабочий стол, чтобы протестировать использование нескольких мониторов на удаленном компьютере, выбрав пункт "Использовать все мои мониторы для удаленного сеанса" на вкладке "Экран", как показано на снимке экрана ниже.

![Приложение "Подключение к удаленному рабочему столу" с открытой вкладкой "Экран" и установленным флажком "Использовать все мои мониторы для удаленного сеанса".](./media/remote-desktop-use-all-monitors.png)

## <a name="see-also"></a>См. также

### <a name="articles"></a>Статьи

- [Разработка приложения WPF с поддержкой dpi для каждого монитора](https://docs.microsoft.com/windows/desktop/hidpi/declaring-managed-apps-dpi-aware) предоставляет общий обзор и руководство по написанию приложений Win32 для настольных ПК. Многие из методов, описанных в этой статье применяются для решений по расширению Office.
- 
  [API для смешанного использования режимов масштабирования и поддержки определения DPI.](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-improvements-for-desktop-applications) Содержит список API, относящихся к разрешению.
- [Руководство для разработчиков — DPI на уровне монитора — просмотр WPF.](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) Содержит руководство по разработке приложения WPF для создания приложений WPF с поддержкой определения DPI.
- [Поддержка мониторов с высоким разрешением в Office.](https://support.office.com/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) Содержит сведения о том, как пользователь может настроить Office для оптимизации обеспечения совместимости, если решение для Office не поддерживается надлежащим образом при изменении разрешения.
- [Изменение масштаба экрана для юбилейного обновления Windows 10.](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) Это запись блога, описывающая изменения, которые добавлены в юбилейном обновлении Windows 10. 
- [Маркер DPI_AWARENESS_CONTEXT](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context). Содержит сведения о значениях и определениях DPI_AWARENESS_CONTEXT для программирования.
- [Разработка классических приложений с высоким разрешением для Windows.](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) Содержит сведения о тестировании в разделе "Тестирование изменений".

### <a name="code-samples"></a>Примеры кода

- [Пример поддержки определения DPI на уровне окна](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow)
- [Пример динамического разрешения](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DynamicDPI)
- [Пример WPF c поддержкой определения на уровне монитора](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
