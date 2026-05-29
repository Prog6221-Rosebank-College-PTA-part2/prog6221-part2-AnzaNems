[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Apa4hIya)
ST10480934
<Window x:Class="CybersecurityChatBot_2.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        Title="CyberGuardChatBot" Height="650" Width="850" MinHeight="500" MinWidth="700">
    <Grid Background="#FF1E1E1E">
        <Grid.Resources>
            <Style x:Key="ModernTextBoxStyle" TargetType="TextBox">
                <Setter Property="Background" Value="#FF3C3C3C"/>
                <Setter Property="Foreground" Value="#FFCCCCCC"/>
                <Setter Property="BorderBrush" Value="#FF00BCD4"/>
                <Setter Property="BorderThickness" Value="1"/>
                <Setter Property="Padding" Value="5"/>
                <Setter Property="VerticalContentAlignment" Value="Center"/>
                <Setter Property="FontSize" Value="13"/>
            </Style>
        </Grid.Resources>
    </Grid>
</Window>
<Style x:Key="ModernButtonStyle" TargetType="Button">
    <Setter Property="Background" Value="#FF00BCD4"/>
    <Setter Property="Foreground" Value="White"/>
    <Setter Property="Template">
        <Setter.Value>
            <ControlTemplate TargetType="Button">
                <Border Background="{TemplateBinding Background}" BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}" CornerRadius="3">
                    <ContentPresenter HorizontalAlignment="Center" VerticalAlignment="Center"/>
                </Border>
            </ControlTemplate>
        </Setter.Value>
    </Setter>
</Style>
<!-- Banner Section -->
        <Border Grid.Row="0" Margin="10,10,10,0" Padding="10" BorderBrush="#FF00BCD4" BorderThickness="1" CornerRadius="5" Background="#FF1E1E1E">
            <TextBlock FontFamily="Consolas" Foreground="Cyan" HorizontalAlignment="Center" TextAlignment="Center" FontSize="10">
                <Run Text="        ██████╗██╗   ██╗██████╗ ███████╗██████╗      "/><LineBreak/>
                <Run Text="       ██╔════╝╚██╗ ██╔╝██╔══██╗██╔════╝██╔══██╗     "/><LineBreak/>
                <Run Text="       ██║      ╚████╔╝ ██████╔╝█████╗  ██████╔╝     "/><LineBreak/>
                <Run Text="       ██║       ╚██╔╝  ██╔══██╗██╔══╝  ██╔══██╗     "/><LineBreak/>
                <Run Text="       ╚██████╗   ██║   ██████╔╝███████╗██║  ██║     "/><LineBreak/>
                <Run Text="        ╚═════╝   ╚═╝   ╚═════╝ ╚══════╝╚═╝  ╚═╝    "/><LineBreak/>
                <LineBreak/>
                <Run Text="        ██████╗ ██╗   ██╗ █████╗ ██████╗ ██████╗     "/><LineBreak/>
                <Run Text="       ██╔════╝ ██║   ██║██╔══██╗██╔══██╗██╔══██╗    "/><LineBreak/>
                <Run Text="       ██║  ███╗██║   ██║███████║██████╔╝██║  ██║    "/><LineBreak/>
                <Run Text="       ██║   ██║██║   ██║██╔══██║██╔══██╗██║  ██║    "/><LineBreak/>
                <Run Text="       ╚██████╔╝╚██████╔╝██║  ██║██║  ██║██████╔╝    "/><LineBreak/>
                <Run Text="        ╚═════╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝    "/><LineBreak/>
                <LineBreak/>
                <Run Text="  [ Cybersecurity Awareness Assistant  v1.0 ]" Foreground="DarkCyan"/>
            </TextBlock>
        </Border>


<Border x:Name="NameEntrySection" Grid.Row="1" Margin="10" Padding="10" BorderBrush="#FF00BCD4" BorderThickness="1" CornerRadius="5" Background="#FF1E1E1E">
    <StackPanel HorizontalAlignment="Center">
        <TextBlock Text="Please enter your name to begin:" HorizontalAlignment="Center" Margin="0,0,0,5" Foreground="#FFCCCCCC"/>
        <TextBox x:Name="UserNameTextBox" Width="250" HorizontalAlignment="Center" Margin="0,0,0,10" Style="{StaticResource ModernTextBoxStyle}" KeyDown="txtName_KeyDown"/>
        <Button x:Name="StartChatButton" Content="Start Chat" Width="120" HorizontalAlignment="Center" Style="{StaticResource ModernButtonStyle}" Click="btnStart_Click"/>
        <TextBlock x:Name="NameErrorTextBlock" Text="" Foreground="Red" HorizontalAlignment="Center" Margin="0,5,0,0" FontWeight="Bold"/>
    </StackPanel>
</Border>
<Border Grid.Row="3" Margin="10,0,10,5" Padding="5" BorderBrush="#FF00BCD4" BorderThickness="1" CornerRadius="5" Background="#FF1E1E1E">
    <StackPanel Orientation="Horizontal" HorizontalAlignment="Center">
        <TextBlock Text="Quick Topics:" VerticalAlignment="Center" Margin="0,0,10,0" FontWeight="Bold" Foreground="#FF00BCD4"/>
        <RadioButton x:Name="PhishingRadioButton" Content="Phishing" GroupName="QuickTopics" Margin="0,0,10,0" Style="{StaticResource ModernRadioButtonStyle}" Checked="TopicRadio_Checked"/>
        <RadioButton x:Name="PasswordRadioButton" Content="Passwords" GroupName="QuickTopics" Margin="0,0,10,0" Style="{StaticResource ModernRadioButtonStyle}" Checked="TopicRadio_Checked"/>
        <RadioButton x:Name="MFARadioButton" Content="MFA" GroupName="QuickTopics" Margin="0,0,10,0" Style="{StaticResource ModernRadioButtonStyle}" Checked="TopicRadio_Checked"/>
    </StackPanel>
</Border>
<Grid Grid.Row="4" Margin="10">
    <Grid.ColumnDefinitions>
        <ColumnDefinition Width="*"/>
        <ColumnDefinition Width="Auto"/>
        <ColumnDefinition Width="Auto"/>
        <ColumnDefinition Width="Auto"/>
    </Grid.ColumnDefinitions>
    <TextBox x:Name="UserInputTextBox" Grid.Column="0" Margin="0,0,10,0" Style="{StaticResource ModernTextBoxStyle}" KeyDown="txtInput_KeyDown"/>
    <Button x:Name="SendButton" Grid.Column="1" Content="Send" Width="75" Margin="0,0,5,0" Style="{StaticResource ModernButtonStyle}" Click="btnSend_Click"/>
    <Button x:Name="ChatHistoryButton" Grid.Column="2" Content="Chat History" Width="100" Margin="0,0,5,0" Style="{StaticResource ModernButtonStyle}" Click="ChatHistoryButton_Click"/>
    <Button x:Name="MuteToggleButton" Grid.Column="3" Content="Mute Voice" Width="100" Style="{StaticResource ModernButtonStyle}" Click="btnSpeak_Click"/>
</Grid>
public class CyberTopic
{
    public string Name { get; set; } = string.Empty;
    public List<string> Steps { get; set; } = new List<string>( );
    public List<string> Tips { get; set; } = new List<string>();
    public List<string> Prevention { get; set; } = new List<string>();
}

public class ChatMessage
{
    public string Sender { get; set; } = string.Empty;
    public string Message { get; set; } = string.Empty;
    public DateTime Timestamp { get; set; }
}
public CyberBotEngine()
{
    _knowledgeBase = new Dictionary<string, CyberTopic>(StringComparer.OrdinalIgnoreCase);
    InitializeKnowledgeBase();
}

private void AddTopic(string key, string name, string[] steps, string[] tips, string[] prevention)
{
    _knowledgeBase[key] = new CyberTopic { 
        Name = name, 
        Steps = steps.ToList(), 
        Tips = tips.ToList(), 
        Prevention = prevention.ToList() 
    };
}
public CyberBotEngine()
{
    _knowledgeBase = new Dictionary<string, CyberTopic>(StringComparer.OrdinalIgnoreCase);
    InitializeKnowledgeBase();
}

private void AddTopic(string key, string name, string[] steps, string[] tips, string[] prevention)
{
    _knowledgeBase[key] = new CyberTopic { 
        Name = name, 
        Steps = steps.ToList(), 
        Tips = tips.ToList(), 
        Prevention = prevention.ToList() 
    };
}
public string GetBotResponse(string input)
{
    string lowerInput = input.ToLower();
    _history.Add(new ChatMessage { Sender = UserName ?? "User", Message = input, Timestamp = DateTime.Now });

    foreach (var topic in _knowledgeBase)
    {
        if (lowerInput.Contains(topic.Key))
        {
            _currentTopicKey = topic.Key;
            return $"I see you're interested in {topic.Value.Name}. {topic.Value.Steps[0]} You can ask for 'tips', 'prevention', or 'more' information on this!";
        }
    }
    return "I'm not sure I understand. Try asking about VPNs, Phishing, or Passwords.";
}
AddTopic("vpn", "VPN (Virtual Private Network)", 
    new[] { "A VPN creates a private, encrypted 'tunnel' across a public network." }, 
    new[] { "Tip: Use a VPN whenever you connect to public Wi-Fi at cafes or airports." },
    new[] { "Prevention: A VPN prevents 'Man-in-the-Middle' attacks on public networks." });
    if (!string.IsNullOrEmpty(_currentTopicKey))
{
    var topic = _knowledgeBase[_currentTopicKey];
    if (lowerInput.Contains("tip")) return topic.Tips[_random.Next(topic.Tips.Count)];
    if (lowerInput.Contains("prevent")) return topic.Prevention[_random.Next(topic.Prevention.Count)];
    if (lowerInput.Contains("more") || lowerInput.Contains("next"))
    {
        var allInfo = topic.Steps.Concat(topic.Tips).Concat(topic.Prevention).ToList();
        return allInfo[_random.Next(allInfo.Count)];
    }
}
public string GetFullChatHistory()
{
    return string.Join("\n", _history.Select(h => $"[{h.Timestamp:HH:mm:ss}] {h.Sender}: {h.Message}"));
}

public void LogMessage(string sender, string message)
{
    _history.Add(new ChatMessage { Sender = sender, Message = message, Timestamp = DateTime.Now });
}
public MainWindow()
{
    InitializeComponent();
    _botEngine = new CyberBotEngine();
    
    try
    {
        _speechSynthesizer = new SpeechSynthesizer();
        _speechSynthesizer.SetOutputToDefaultAudioDevice();
    }
    catch { _speechSynthesizer = null; }

    DisplayWelcomeScreen();
    ToggleChatControls(false);
}
private void btnStart_Click(object sender, RoutedEventArgs e)
{
    string name = UserNameTextBox.Text.Trim();
    if (string.IsNullOrWhiteSpace(name) || !Regex.IsMatch(name, "^[a-zA-Z][a-zA-Z ]*$"))
    {
        NameErrorTextBlock.Text = "Please enter a valid name (letters only).";
        Speak("Please enter a valid name.");
    }
    else
    {
        _botEngine.UserName = name;
        NameEntrySection.Visibility = Visibility.Collapsed;
        ToggleChatControls(true);
        AppendBotMessage($"Hello {_botEngine.UserName}!", Brushes.Cyan, true);
    }
}
private void ProcessInput()
{
    string input = UserInputTextBox.Text.Trim();
    if (string.IsNullOrWhiteSpace(input)) return;

    AppendUserMessage(input);
    string response = _botEngine.GetBotResponse(input);
    AppendBotMessage(response, Brushes.Cyan, true);
    Speak(response);
    UserInputTextBox.Clear();
}
private void txtInput_KeyDown(object sender, System.Windows.Input.KeyEventArgs e) 
{ 
    if (e.Key == System.Windows.Input.Key.Enter) ProcessInput(); 
}

private void txtName_KeyDown(object sender, System.Windows.Input.KeyEventArgs e) 
{ 
    if (e.Key == System.Windows.Input.Key.Enter) btnStart_Click(sender, e); 
}
private void TopicRadio_Checked(object sender, RoutedEventArgs e) 
{ 
    if (sender is RadioButton rb && rb.IsChecked == true) 
    { 
        UserInputTextBox.Text = rb.Content.ToString(); 
        ProcessInput(); 
        rb.IsChecked = false; 
    } 
}
private void ToggleChatControls(bool enable)
{
    UserInputTextBox.IsEnabled = enable;
    SendButton.IsEnabled = enable;
    ChatHistoryButton.IsEnabled = enable;
    PhishingRadioButton.IsEnabled = enable;
    PasswordRadioButton.IsEnabled = enable;
    MFARadioButton.IsEnabled = enable;
}
private void ToggleChatControls(bool enable)
{
    UserInputTextBox.IsEnabled = enable;
    SendButton.IsEnabled = enable;
    ChatHistoryButton.IsEnabled = enable;
    PhishingRadioButton.IsEnabled = enable;
    PasswordRadioButton.IsEnabled = enable;
    MFARadioButton.IsEnabled = enable;
}
try
{
    _speechSynthesizer = new SpeechSynthesizer();
    _speechSynthesizer.SetOutputToDefaultAudioDevice();
}
catch { _speechSynthesizer = null; }
private void Speak(string text)
{
    if (_speechSynthesizer != null && !_isMuted)
    {
        try { _speechSynthesizer.SpeakAsync(text); } catch { }
    }
}
private void btnSpeak_Click(object sender, RoutedEventArgs e)
{
    if (_speechSynthesizer != null)
    {
        if (_isMuted) _speechSynthesizer.Volume = 100;
        else
        {
            _speechSynthesizer.SpeakAsyncCancelAll();
            _speechSynthesizer.Volume = 0;
        }
        _isMuted = !_isMuted;
    }
}
if (_isMuted)
{
    MuteToggleButton.Content = "Mute Voice";
}
else
{
    MuteToggleButton.Content = "Unmute Voice";
}
private void ProcessInput()
{
    // ... logic ...
    _speechSynthesizer?.SpeakAsyncCancelAll();
    Speak(response);
}
private void Speak(string text)
{
    if (_speechSynthesizer == null) return; // Silent fail if no device
    try { _speechSynthesizer.SpeakAsync(text); } catch { }
}
private void AppendBotMessage(string message, SolidColorBrush color, bool log)
{
    Dispatcher.Invoke(() => {
        TextRange tr = new TextRange(ChatDisplay.Document.ContentEnd, ChatDisplay.Document.ContentEnd);
        tr.Text = "🤖 CyberGuard » " + message + "\n\n";
        tr.ApplyPropertyValue(TextElement.ForegroundProperty, color);
        ChatDisplay.ScrollToEnd();
        if (log) _botEngine.LogMessage("CyberGuard", message);
    });
}
private void AppendUserMessage(string message)
{
    Dispatcher.Invoke(() => {
        TextRange tr = new TextRange(ChatDisplay.Document.ContentEnd, ChatDisplay.Document.ContentEnd);
        tr.Text = "👤 You » " + message + "\n\n";
        tr.ApplyPropertyValue(TextElement.ForegroundProperty, Brushes.LightGreen);
        ChatDisplay.ScrollToEnd();
        _botEngine.LogMessage(_botEngine.UserName ?? "User", message);
    });
}
private void ChatHistoryButton_Click(object sender, RoutedEventArgs e)
{
    string fullHistory = _botEngine.GetFullChatHistory();
    Window historyWindow = new Window
    {
        Title = "Full Chat History Report",
        Width = 600,
        Height = 500,
        WindowStartupLocation = WindowStartupLocation.CenterScreen,
        Background = new SolidColorBrush(Color.FromRgb(30, 30, 30))
    };
    historyWindow.ShowDialog();
}
TextBox historyBox = new TextBox
{
    Text = fullHistory,
    IsReadOnly = true,
    VerticalScrollBarVisibility = ScrollBarVisibility.Auto,
    Background = new SolidColorBrush(Color.FromRgb(45, 45, 48)),
    Foreground = Brushes.LightGray,
    FontFamily = new FontFamily("Consolas"),
    Padding = new Thickness(10),
    TextWrapping = TextWrapping.Wrap
};
historyWindow.Content = historyBox;
public string GetFullChatHistory()
{
    return string.Join("\n", _history.Select(h => $"[{h.Timestamp:HH:mm:ss}] {h.Sender}: {h.Message}"));
}
private void AppendBotMessage(string message, SolidColorBrush color, bool log)
{
    // ... append logic ...
    ChatDisplay.ScrollToEnd();
}
