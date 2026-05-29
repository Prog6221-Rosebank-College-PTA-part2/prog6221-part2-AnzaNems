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
